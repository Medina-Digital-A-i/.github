# Running a persistent, multi-agent "AI company" with Claude as the brain — landscape as of 21 Oct 2026

Prepared for a solo founder with: an always-on Mac mini, one or more MacBooks, and Claude cloud sessions. Every claim is sourced; anything I could not confirm against a primary source is tagged **[unverified]**. Prices are list prices per million tokens (MTok) unless stated.

---

## 0. Executive summary and recommended stack

**The short version.** In October 2026 Anthropic's own product surface already covers most of what a one-person "AI company" needs, and it does so with better security defaults than the self-hosted personal-agent projects. The recommended architecture is:

1. **Brain / CEO:** Claude Opus 5.5 (default in Claude Code on Pro/Max; $4/$20) with Claude Fable 5.1 ($10/$50) reserved for the hardest planning and review work. [Models overview](https://platform.claude.com/docs/en/about-claude/models/overview)
2. **Durable memory = a git repo, not a chat history.** One private "company" repo holding `CLAUDE.md` (constitution), `.claude/rules/` (per-area policies), `.claude/skills/` (SOPs), `.claude/agents/` (role definitions with `memory: project`), and `docs/` (decisions, OKRs, run logs). Everything that must survive a session gets written to a file and committed. Claude Code's auto memory and Projects' memory are useful but machine-local or product-local, respectively. [Memory docs](https://code.claude.com/docs/en/memory), [Subagent memory](https://code.claude.com/docs/en/sub-agents)
3. **Scheduling:** Anthropic cloud scheduled tasks (formerly "routines") for anything that must run even if the Mac mini is off (min interval 1 hour; API and GitHub-event triggers), Desktop scheduled tasks on the Mac mini for anything that needs local files (min interval 1 minute). [Scheduled tasks](https://code.claude.com/docs/en/routines), [Desktop scheduled tasks](https://code.claude.com/docs/en/desktop-scheduled-tasks)
4. **Mac mini role:** a Claude Code "server" (`claude remote-control --spawn worktree`) that you drive from your phone, plus Channels (Telegram/Discord/iMessage) so events and chat messages push into a live session, plus Ollama for cheap local triage. Keep OpenClaw off the primary machine, or run it only in a sandbox after reading its security history. [Remote Control](https://code.claude.com/docs/en/remote-control), [Channels](https://code.claude.com/docs/en/channels)
5. **Workers:** Claude Code subagents (fresh context, up to 20 concurrent, 3 levels deep) for parallel work; Agent Teams only for research/debate tasks (experimental, ~7x tokens). Haiku 5.5 ($0.10/$0.50) for classification, routing and subagent grunt work. [Sub-agents](https://code.claude.com/docs/en/sub-agents), [Agent teams](https://code.claude.com/docs/en/agent-teams)
6. **Second-opinion / specialist models via API:** GPT-6.1 Sol ($2/$10) as a cross-check reviewer, Gemini 3.8 Flash ($0.75/$3.75) for cheap long-context and multimodal grunt work, DeepSeek V4.1 Flash ($0.30/$1.20) for bulk cheap text, Qwen3.8-27B or Muse Glimmer locally for free offline tasks.
7. **Glue:** n8n (self-hosted, native MCP server) or Zapier MCP for SaaS plumbing; the Claude Agent SDK only if you outgrow Claude Code and need a custom harness; Managed Agents (beta, $0.08/session-hour + tokens) if you want Anthropic to host the long-running agents with memory stores and "dreaming" consolidation.

**Budget expectation:** Anthropic reports ~$13/active day and $150–250/month per developer on API billing; a Max 20x subscription ($200/mo) with usage credits is the cheaper, simpler path for one person until you exceed it. [Costs](https://code.claude.com/docs/en/costs)

---

## 1. The Claude ecosystem (October 2026)

### 1.1 Current models (official)

| Model | API ID | Price in/out | Context / max out | Note |
|---|---|---|---|---|
| Claude Fable 5.1 | `claude-fable-5-1` | $10 / $50 | 1M / 128K | "Demanding reasoning and long-horizon agentic work." Same weights as restricted Mythos 5.1 minus cyber/bio safeguard lifts. Cache read 2.5% of input. |
| Claude Opus 5.5 | `claude-opus-5-5` | $4 / $20 | 1M / 128K | Released 22 Sep 2026; "performs at the level of Fable 5.1 on most work, 40% cheaper than Opus 5." Default in Claude Code. Fast mode $8/$40. |
| Claude Sonnet 5.5 | `claude-sonnet-5-5` | $2 / $10 | 1M / 128K | Released 28 Sep 2026. |
| Claude Haiku 5.5 | `claude-haiku-5-5` | $0.10 / $0.50 (≤100K prompt); $0.50/$2.50 above | 1M / 128K | Released 7 Oct 2026; "built for summarization, subagents, and browser use." |

Sources: [Models overview](https://platform.claude.com/docs/en/about-claude/models/overview), [Pricing](https://platform.claude.com/docs/en/about-claude/pricing), [Opus 5.5 announcement](https://www.anthropic.com/news/claude-opus-5-5), [Anthropic news index](https://www.anthropic.com/news). All current models have adaptive thinking that cannot be turned off; knowledge cutoff June 2026; batch is 50% off; web search $10/1,000 searches; web fetch free beyond tokens.

### 1.2 Claude Code — the surfaces

Claude Code is now one harness exposed through: terminal CLI, VS Code/JetBrains, the Desktop app (macOS, Windows, Linux beta), claude.ai/code cloud sessions, the mobile app (via Remote Control and cloud sessions), and Slack. The October 2026 release train is at v2.1.30x; recent additions: **mods** (TypeScript plugins that can add panes, rewrite prompts, intercept tool calls), **server-side auto mode** on by default (a classifier screens each action; its calls don't count against limits), **`/goal`** (autonomous until a condition is met), **dynamic workflows** (hundreds of parallel subagents), **`/schedule`**, and **Projects**. [Changelog](https://code.claude.com/docs/en/changelog), [Oct 2026 cheat sheet](https://dev.to/anglo_lima/claude-code-cheat-sheet-october-2026-the-complete-state-of-play-1j26), [2026 launch timeline](https://linas.substack.com/p/anthropic-claude-2026-every-launch-guide)

#### Memory: what actually persists

| Mechanism | Who writes | Scope / location | Loaded when | Persists across machines? |
|---|---|---|---|---|
| `CLAUDE.md` / `CLAUDE.local.md` / `~/.claude/CLAUDE.md` | You | Repo (committed), repo (gitignored), user | Every session, in full (target <200 lines; 4 MiB hard cap) | Yes if committed |
| `.claude/rules/*.md` | You | Repo or `~/.claude/rules/`; path-scoped rules load on demand | On match | Yes if committed |
| `AGENTS.md` | You | Repo; read when no CLAUDE.md exists (or both, via setting) | Every session | Yes |
| **Auto memory** | Claude | `~/.claude/projects/<repo>/memory/MEMORY.md` + topic files; four note types (user, feedback, project, reference) | First 200 lines / 25 KB of MEMORY.md at start; topic files on demand | **No** — "machine-local… not shared across machines or cloud environments." Relocatable with `autoMemoryDirectory` (point it inside a synced/committed folder). |
| **Subagent memory** (`memory: project`) | Subagent | `.claude/agent-memory/<agent>/` (committed), `user`, or `local` | First 200 lines / 25 KB of its MEMORY.md | Yes if `project` scope and committed |
| **Project memory** (Claude Code Projects) | Claude | Inside the claude.ai project; `MEMORY.md` index read by every cloud thread | Every cloud thread | Product-local; not loaded into threads you run on your own machine via Remote Control |
| Session transcripts | Claude Code | `~/.claude/projects/<cwd>/*.jsonl`; `--resume`, `--continue`, fork | Only when resumed | No (SDK `SessionStore` can mirror) |
| Cloud session sandbox | — | Fresh clone each run | — | No |

Sources: [Memory](https://code.claude.com/docs/en/memory), [Sub-agents](https://code.claude.com/docs/en/sub-agents), [Projects](https://code.claude.com/docs/en/claude-projects), [Agent SDK sessions](https://code.claude.com/docs/en/agent-sdk/sessions). Key quote from the docs: "Each Claude Code session begins with a fresh context window." Memory files are "context, not enforced configuration" — to hard-block an action use a `PreToolUse` hook.

#### Scheduling: three tiers

| | Cloud scheduled task (was "routine") | Desktop scheduled task | `/loop` (session-scoped) |
|---|---|---|---|
| Runs on | Anthropic cloud (or self-hosted env) | Your Mac (app open, awake) | Your Mac, inside an open session |
| Triggers | Cron (min 1 h), one-off, **API POST with bearer token**, **GitHub PR/release events** | Hourly/daily/weekly/custom cron (min 1 min) | Cron (min 1 min), self-paced; expires after 7 days |
| Local files | No (fresh clone) | Yes | Yes |
| Permissions | Runs autonomously, no prompts | Per-task mode; "always allow" after first run | Inherits session |
| Limits | 100 scheduled runs/hour per account; runs count against plan usage; task owned by your personal account | Missed runs: one catch-up on wake | 50 tasks/session |
| Plans | Pro, Max, Team, Enterprise | Desktop ≥1.1.5368 | any |

Sources: [Scheduled tasks](https://code.claude.com/docs/en/routines), [Desktop scheduled tasks](https://code.claude.com/docs/en/desktop-scheduled-tasks), [/loop](https://code.claude.com/docs/en/scheduled-tasks). Scheduled tasks are still labelled "research preview." Fire-payload text arrives wrapped as untrusted data; your prompt must explicitly opt in to acting on it.

#### Projects (public beta, Pro/Max only)
One coordinating conversation spawns parallel cloud "threads," each a full cloud session sharing repositories, 16,000-char project instructions, and project memory. Threads run in auto mode; 200 new threads/day cap; threads can run on your own machine via Remote Control when they need local resources. Not on Team/Enterprise yet; not in the terminal. [Projects](https://code.claude.com/docs/en/claude-projects)

#### Subagents, Agent Teams, cross-session messaging, Channels, Remote Control
- **Subagents:** fresh context each; background by default; up to 20 concurrent; nest 3 deep; `isolation: worktree`; per-agent model (`haiku` for cheap tasks); persistent memory via `memory:` frontmatter. They do **not** see the parent's conversation, auto memory, or skills unless passed in the delegation prompt. [Sub-agents](https://code.claude.com/docs/en/sub-agents)
- **Agent Teams:** experimental (`CLAUDE_CODE_EXPERIMENTAL_AGENT_TEAMS=1`), lead + teammates with a file-locked shared task list and mailboxes under `~/.claude/teams/`. Not resumable, one team per session, no nesting, "approximately 7x more tokens." Best for research/review/competing hypotheses. [Agent teams](https://code.claude.com/docs/en/agent-teams), [Costs](https://code.claude.com/docs/en/costs)
- **Cross-session messaging:** any of your sessions (same machine, other machine via Remote Control, or cloud) can message another; messages are plain text, never count as consent, and loops are throttled. [Cross-session messaging](https://code.claude.com/docs/en/cross-session-messaging)
- **Channels (research preview):** MCP plugins that push Telegram/Discord/iMessage messages or webhooks into a *running* session; two-way; sender allowlist by pairing code; `-p` mode supported for unattended workers. "For an always-on setup you run Claude in a background process or persistent terminal." [Channels](https://code.claude.com/docs/en/channels)
- **Remote Control:** `claude remote-control` turns a local folder into a server you drive from claude.ai or the mobile app; `--spawn worktree`, `--capacity 32`; auto-reconnects after sleep; Pro/Max/Team/Enterprise, no API keys; optional Trusted Devices. [Remote Control](https://code.claude.com/docs/en/remote-control)

#### Skills, hooks, MCP, plugins, Chrome
- **Skills** (`SKILL.md` with frontmatter) load on demand; `/skill-doctor` flags unused context hogs; subagents preload at most 32 skills. Official marketplace `claude-plugins-official` (~300 plugins; count varies by date) plus the public Skills Marketplace launched 1 May 2026 with ~600 skills. Third-party directories: [awesomeclaude.ai](https://awesomeclaude.ai/awesome-claude-skills), [claudemarketplaces.com](https://claudemarketplaces.com/), [claudemarketplace.net](https://www.claudemarketplace.net/). [Plugins guide](https://designrevision.com/blog/claude-code-plugins), [Skills directory comparison](https://localskills.sh/blog/claude-skills-marketplace-guide)
- **Hooks:** 33 events, 5 handler types, `onFailure: "block"`; `TeammateIdle`, `TaskCreated`, `TaskCompleted` gates for teams. [Changelog](https://code.claude.com/docs/en/changelog)
- **MCP:** connectors you add at claude.ai/customize/connectors are available to cloud sessions and scheduled tasks; local `claude mcp add` servers are not. Tool definitions are deferred by default to save context. [Scheduled tasks → Connectors](https://code.claude.com/docs/en/routines)
- **Claude in Chrome:** generally available on all paid plans (date reported as 26 Aug 2026 by secondary sources; the Oct cheat sheet says "since July") — **[date unverified]**; Chrome desktop only; callable from Claude Code and Cowork. [fast.io guide](https://fast.io/resources/claude-browser-extension-guide/), [clickforest](https://www.clickforest.com/en/blog/claude-in-chrome-explained)

### 1.3 Claude Cowork → "one Claude"
Cowork (Jan 2026 preview, GA 9 Apr 2026) was merged into the main Claude app on **16 Sep 2026**: "Cowork and Design capabilities are now available from any conversation," rolling out first to Pro/Max on web, desktop and mobile; tasks "continue even after you've closed your laptop"; recurring scheduled work is supported; an opt-in mode works autonomously and only checks in when needed. Local-file and computer-control tasks still need the desktop app. [claude.com blog](https://claude.com/blog/cowork-is-now-claude), [support article](https://support.claude.com/en/articles/16761823-claude-cowork-and-chat-are-one-claude), [igeeksblog](https://www.igeeksblog.com/claude-cowork-chat-merge/)

### 1.4 Claude Agent SDK
Same harness as Claude Code as a Python/TypeScript library. Sessions persist to `~/.claude/projects/<cwd>/*.jsonl`; `continue`, `resume`, `fork`; `SessionStore` adapter mirrors transcripts to your backend for cross-host resume; file checkpointing; `max_turns` and `max_budget_usd` caps. The SDK has **no built-in cross-session memory** — you supply it (files, DB, Mem0). Spawning agent-team teammates is not supported in `-p`/SDK mode. [Agent SDK sessions](https://code.claude.com/docs/en/agent-sdk/sessions), [SDK overview](https://code.claude.com/docs/en/agent-sdk/overview)

### 1.5 Claude Managed Agents (public beta since 9 Apr 2026)
Anthropic-hosted agent harness: Agents (model+prompt+tools+MCP+skills), Environments (cloud or self-hosted sandbox), Sessions (stateful, resumable, server-side history), Events. Add-ons: **memory stores**, **vaults** (credentials), **outcomes**, **multi-agent orchestration**, **scheduled deployments** (cron with timezone, per-run budget cap, up to 1,000 per org), **MCP tunnels** and **Dreams** (research preview: an async job that reads a memory store plus up to 100 session transcripts and emits a deduplicated, reorganized store; billed at normal token rates; minutes to hours). Pricing: tokens at list price + **$0.08 per session-hour**, idle not billed. Not ZDR/HIPAA-eligible because sessions are stored server-side. [Overview](https://platform.claude.com/docs/en/managed-agents/overview), [Dreams](https://platform.claude.com/docs/en/managed-agents/dreams), [Scheduled deployments](https://platform.claude.com/docs/en/managed-agents/scheduled-deployments), [Pricing](https://platform.claude.com/docs/en/about-claude/pricing), [SiliconANGLE](https://siliconangle.com/2026/04/08/anthropic-launches-claude-managed-agents-speed-ai-agent-development/)

### 1.6 Claude in Slack
Two things exist. **Claude Tag** (beta from 23 Jun 2026) is the org-level shared `@Claude` with channel memory, ambient monitoring, and an August update that removed the per-message classifier so it reads full channel context and can "jump in unprompted." It is **Team and Enterprise only** — not Pro/Max. The older per-user **Claude Code in Slack** still works for Pro/Max accounts in workspaces not connected to Tag and spawns a cloud session from an `@Claude` mention; the legacy bot is retired in Tag-connected workspaces effective 5 Oct 2026. [Claude Code in Slack](https://code.claude.com/docs/en/slack), [Claude Tag overview](https://claude.com/docs/claude-tag/overview), [VentureBeat](https://venturebeat.com/orchestration/anthropics-new-claude-tag-update-lets-its-slack-agent-read-the-full-conversation-and-jump-in-unprompted), [TechRepublic](https://www.techrepublic.com/article/news-anthropic-claude-tag-ai-agent-slack/)

### 1.7 Best practices for durable memory (synthesis)
1. **Repo as the single source of truth.** Keep `CLAUDE.md` short (<200 lines), push specifics into `.claude/rules/` (path-scoped) and skills (loaded on demand), and keep a `docs/decisions/` ADR-style log that agents append to. Everything a cloud session or a teammate needs must be committed, because cloud sessions start from a fresh clone and subagents don't inherit auto memory. [Memory](https://code.claude.com/docs/en/memory), [Context engineering](https://www.anthropic.com/engineering/effective-context-engineering-for-ai-agents)
2. **Make auto memory portable.** Set `autoMemoryDirectory` to a folder inside a synced repo (or iCloud/Syncthing) so the Mac mini and MacBooks share it; give role subagents `memory: project` so their learnings are versioned.
3. **Structured note-taking over long transcripts.** Anthropic's guidance: agents should write progress to NOTES/MEMORY files and reload them after compaction; subagents return 1–2K-token summaries. Focused ~300-token prompts beat 113K-token dumps on LongMemEval across every model family (Chroma's "context rot" study, 18 models). [Context engineering](https://www.anthropic.com/engineering/effective-context-engineering-for-ai-agents), [Context rot](https://www.trychroma.com/research/context-rot)
4. **External stores, when you need search over history:**
   - **Mem0** — open-source library + hosted platform; Claude Code integration guide exists; its local "OpenMemory" MCP server was sunset (announced Apr 2026, removed 29 Jul 2026), so use the hosted MCP endpoint or self-host the library/Docker stack. Free tier ~10k ops/month per secondary sources. [Mem0 docs](https://docs.mem0.ai/), [MCP memory servers compared](https://coworker.ai/blog/best-mcp-memory-servers)
   - **Obsidian** — no official AI feature; the Local REST API plugin now bundles an MCP server; `basic-memory` bridges Claude Code and an Obsidian vault (markdown = human-readable and git-friendly). [agentsroom](https://agentsroom.dev/blog/ai-agent-memory-solutions), [mnemoverse comparison](https://mnemoverse.com/docs/library/memory-mcp-servers-compared)
   - **Notion** — community `notion-memory-mcp` uses Notion as the human-editable tier with Mem0/vector DB for recall. [GitHub](https://github.com/shahjalal2313/notion-memory-mcp)
   - **Vector DBs** (Chroma, LanceDB, pgvector) only for large corpora; for a one-person company, grep over markdown plus Claude's 1M context usually suffices.
   - **Managed Agents memory stores + Dreams** if you move the brain to Anthropic's hosted harness. [Dreams](https://platform.claude.com/docs/en/managed-agents/dreams)
5. **Hard rules go in hooks, not memory.** Memory is advisory; `PreToolUse` hooks and permission deny rules are enforced.

---

## 2. Always-on agent host on a Mac mini

### 2.1 Option A (recommended): Claude Code as the resident daemon
- `claude remote-control --spawn worktree --capacity 8` in the company repo, launched by a LaunchAgent, gives you a phone-controllable, multi-session server that reconnects after sleep. [Remote Control](https://code.claude.com/docs/en/remote-control)
- Add `--channels plugin:telegram@claude-plugins-official` (or iMessage, which needs no bot token on macOS) so you can text the company from anywhere and so webhooks (Stripe, GitHub, monitoring) land in a live session. [Channels](https://code.claude.com/docs/en/channels)
- Desktop scheduled tasks for local-file jobs (daily brief pulling from Calendar/Mail connectors, nightly bookkeeping); cloud scheduled tasks for everything else so a Mac mini outage doesn't stop the company.
- Keep-awake: `sudo pmset -c sleep 0 displaysleep 0` plus a LaunchDaemon running `/usr/bin/caffeinate -dimsu` with `KeepAlive` as a safety net (needed at the login screen because macOS sleeps when no user is logged in); verify with `pmset -g assertions`. Desktop app also has "Keep computer awake." [Headless Mac guide](https://www.agileguy.ca/content/files/2026/03/headless-mac-guide.html), [Medium walkthrough](https://chawlaharshit.medium.com/how-i-turned-my-mac-into-a-headless-server-my-always-on-setup-for-ai-monitoring-and-automation-aa9a8ff9aeff), [caffeinate reference](https://myunix.org/macos/macos-caffeinate-pmset/)
- Unattended `-p` workers: start with `crossSessionInbound: accept` in `--settings` so peer messages aren't held for a dialog nobody will answer. [Cross-session messaging](https://code.claude.com/docs/en/cross-session-messaging)

### 2.2 Option B: OpenClaw (ex-Clawdbot / Moltbot)
What it is: MIT-licensed, Node-based self-hosted gateway (~393k GitHub stars) connecting WhatsApp/Telegram/Signal/Slack/Discord to an agent that runs on your hardware; pluggable model providers (Claude, Codex, local); macOS/iOS/Android companion apps; created by Peter Steinberger; renamed after Anthropic objected to "Clawd." It is the project that triggered the 2026 Mac mini buying wave. [GitHub](https://github.com/openclaw/openclaw), [Docs](https://docs.openclaw.ai/), [Lightning AI explainer](https://lightning.ai/blog/what-is-openclaw-clawdbot-moltbot), [Scientific American](https://www.scientificamerican.com/article/moltbot-is-an-open-source-ai-agent-that-runs-your-computer/)

Security record (why it is not the default here):
- CVE-2026-25253 one-click RCE (patched 2026.1.29); CVE-2026-32922 CVSS 9.9 privilege escalation (patched 2026.3.11); four-CVE "Claw Chain" (patched 2026.4.22); two high-severity advisories fixed in 2026.8.1. [ProArch](https://www.proarch.com/blog/threats-vulnerabilities/openclaw-rce-vulnerability-cve-2026-25253), [ARMO](https://www.armosec.io/blog/cve-2026-32922-openclaw-privilege-escalation-cloud-security/), [CSA research note](https://labs.cloudsecurityalliance.org/research/csa-research-note-openclaw-claw-chain-cve-20260517-csa-style/)
- Tens of thousands of internet-exposed instances (40k in Feb per SecurityScorecard; later scans claim far more — counts vary by scanner **[figures approximate]**), often because the gateway bound to `0.0.0.0:18789` by default. [Sangfor](https://www.sangfor.com/blog/cybersecurity/openclaw-ai-agent-security-risks-2026), [Hive Security](https://hivesecurity.gitlab.io/blog/openclaw-ai-agent-security-crisis-2026/)
- "ClawHavoc": 1,184–1,400+ malicious skills on ClawHub including macOS infostealers disguised as Gmail/Notion/Slack integrations; Moltbook leak of ~1.5M API tokens; Microsoft stated it is "not appropriate to run it on a standard personal or corporate machine"; a Meta alignment director's agent mass-deleted real Gmail after compaction dropped her instruction. [BetterClaw timeline](https://www.betterclaw.io/blog/openclaw-security-2026), [Cyberdesserts](https://blog.cyberdesserts.com/openclaw-malicious-skills-security/)
- If you run it anyway: latest release (≥2026.8.1), gateway bound to loopback, dedicated machine or VM, `allowFrom` allowlists, `requireMention` in groups, audit every skill, inspect `SOUL.md`/`MEMORY.md` for injected instructions, require approval for delete/send/pay, rotate all credentials it has touched. [Docs security guidance](https://docs.openclaw.ai/), [BetterClaw hardening](https://www.betterclaw.io/blog/openclaw-security-2026)

### 2.3 Other self-hosted personal agents
- **Hermes Agent** (Nous Research, MIT, ~256k stars): messaging-first (Telegram/Discord/Slack/WhatsApp/Signal), subagents, cron, seven execution backends incl. Docker/SSH, self-curated memory with FTS5 search, OpenClaw migration command; providers via Nous Portal/OpenRouter/OpenAI/custom endpoints (Anthropic direct not listed on the README — **[verify]**). [GitHub](https://github.com/NousResearch/hermes-agent)
- **NanoClaw** (container-sandboxed by default), **ZeroClaw** (lightweight, Raspberry-Pi class). Rankings come from vendor blogs — check the repos. [Composio roundup](https://composio.dev/content/openclaw-alternatives), [Bito roundup](https://bito.ai/ai-tools/openclaw-alternatives/)
- **Perplexity "Personal Computer"**: a Mac mini-resident companion to Perplexity Computer (cloud agent routing across ~19 models); launched 16 Apr 2026 for Max ($200/mo), extended to Pro/Enterprise 7 May 2026 with a native Mac app. [heise](https://heise.de/-11209925), [letsdatascience](https://letsdatascience.com/news/perplexity-turns-mac-mini-into-local-ai-agent-83b6fcf8), [buildfastwithai](https://www.buildfastwithai.com/blogs/what-is-perplexity-computer)

### 2.4 Local models on Apple Silicon (2026)
- **Runtimes:** Ollama is MLX-powered on Apple Silicon (preview 30 Mar 2026; June 2026 update "up to 20% faster," NVFP4 support, agent-oriented caching); Ollama recommends >32 GB unified memory for the MLX path. LM Studio supports both llama.cpp and MLX engines with a GUI and OpenAI-compatible API. Raw `mlx-lm` is fastest but Python-only. Since 25 Aug 2026 Claude Desktop can use Ollama as a third-party gateway provider. Whether MLX is now Ollama's *default* engine is **[unverified]**. [Ollama MLX preview](https://registry.ollama.ai/blog/mlx), [Ollama MLX performance](https://registry.ollama.ai/blog/mlx-performance), [9to5Mac](https://9to5mac.com/2026/03/31/ollama-adopts-mlx-for-faster-ai-performance-on-apple-silicon-macs/), [Ollama blog](https://ollama.com/blog)
- **Models worth running (by unified memory):**
  - 16 GB: gpt-oss-20b (~14 GB), small Gemma 4.
  - 24–32 GB: **Qwen3.6-27B** (dense, Apache-2.0, ~18 GB; 77.2 SWE-bench Verified per secondary sources), Qwen3.6-35B-A3B (MoE, 3B active, very fast), Gemma 4 26B-A4B (multimodal), **Meta Muse Glimmer 30B** (Apache-2.0, multimodal, "designed for local coding agents," `muse-glimmer:30b-mlx`, DFlash 1.5–1.8x faster on Apple Silicon), NVIDIA Nemotron 3.5 Lightning 30B-A3B (tool-calling agents).
  - 48–64 GB: Llama 3.3 70B quantized (older but solid), **Qwen3.8-27B** (Apache-2.0, 262K context, Aug 2026).
  - 128 GB+: the big MoEs (DeepSeek V4.1 Flash ~552B, Kimi K3 2.8T, Qwen3.8-2.4T) are datacenter-class; not practical on a Mac mini.
  Sources: [Analytics Vidhya](https://www.analyticsvidhya.com/blog/2026/09/best-local-llms-mac-mini-2026/), [insiderllm](https://insiderllm.com/guides/best-local-llms-mac-2026/), [Ollama Muse Glimmer](https://ollama.com/blog/muse-glimmer), [the-decoder on Qwen3.8](https://the-decoder.com/alibabas-qwen-team-releases-qwen-3-8-models-with-open-weights-under-the-apache-2-0-license/), [mindstudio open-source coding](https://www.mindstudio.ai/blog/best-open-source-llms-agentic-coding-2026)
- **What local is actually good for in this setup:** PII-sensitive triage (email/CRM classification), first-pass summarization, embedding/search, and "is this worth waking the paid model?" gating. Frontier-quality agentic coding and planning still belong to hosted models.

---

## 3. Other frontier models and tools — what each is best for

### 3.1 OpenAI
- **Models (API, Oct 2026):** GPT-6 Astra $10/$50 (launched 3 Sep 2026), GPT-6 Sol and GPT-6 Luna (22 Sep; $2/$10 and $0.10/$0.50), GPT-6.1 Sol (29 Sep; $2/$10, "near-Astra performance for complex, long-running work"), GPT-6.1 Sol Ultrafast for Pro $500/Enterprise. GPT-5.5 ($5/$30) was retired from ChatGPT/Codex on 14 Oct 2026 but remains on the API. gpt-5.3-codex $1.75/$14 is the listed coding specialist. [OpenAI pricing](https://developers.openai.com/api/docs/pricing), [ChatGPT & Codex changelog](https://learn.chatgpt.com/docs/changelog)
- **Agent products:** "Operator" was retired Aug 2025 into ChatGPT agent, which was itself folded into **ChatGPT Work** (launched 9 Jul 2026): an agentic mode across connected apps/files, local or cloud execution, approval checkpoints. **Pulse** was replaced by **Scheduled Tasks** (17 Jun 2026, hourly minimum). Codex CLI/app continue (MCP-server command removed 5 Sep 2026). [TNW on ChatGPT Work](https://thenextweb.com/news/openai-chatgpt-work-agent-launch), [9to5Mac on scheduled tasks](https://9to5mac.com/2026/06/17/openai-launches-scheduled-tasks-in-chatgpt-details-here/), [Wikipedia: Operator](https://en.wikipedia.org/wiki/OpenAI_Operator)
- **Best used for:** independent second-opinion code review and planning critique (different failure modes from Claude), cheap bulk work with Luna, and anything that needs OpenAI-only integrations.

### 3.2 Google
- **Models:** Gemini 3.5 Flash (I/O, 19 May 2026) → 3.6 → 3.7 → **3.8 Flash** (2 Sep 2026, "long-horizon software engineering and autonomous agents," $0.75/$3.75 intro through 31 Dec 2026, free tier available) → **Gemini 4 Argon** GA 13 Oct 2026 ($2/$10 intro, $4/$20 from 1 Dec 2026, no free tier). 3.8 Live / TTS GA for voice agents; Nano Banana 2.1 for images. [Gemini API changelog via Releasebot](https://releasebot.io/updates/google/gemini-api), [Gemini pricing](https://ai.google.dev/gemini-api/docs/pricing), [Google I/O 2026](https://blog.google/innovation-and-ai/technology/developers-tools/google-io-2026-developer-highlights/)
- **Tools:** Gemini CLI was retired for individuals on 18 Jun 2026 in favour of **Antigravity CLI (`agy`)**, part of Antigravity 2.0 (desktop multi-agent orchestrator with scheduled background tasks, IDE, Python SDK). Antigravity also runs Claude Sonnet/Opus 5.5 on Pro/Ultra. Google AI Pro $20/mo, Ultra $100–200/mo; Gemini API Managed Agents (Interactions API) give hosted sandboxes. [GitHub transition notice](https://github.com/google-gemini/gemini-cli/discussions/27274), [Layer3 Antigravity guide](https://www.layer3labs.io/guides/google-antigravity-explained)
- **Best used for:** cheapest strong multimodal/long-context worker (3.8 Flash on the free tier for dev), video/audio understanding, voice agents, Google Workspace-native automation.

### 3.3 Meta — "Meta Muse"
The user most likely means **Muse Spark**, Meta's first model from Meta Superintelligence Labs (8 Apr 2026): natively multimodal reasoning (voice/text/image in, text out), tool use, "multi-agent orchestration," cloud-only, powering the Meta AI app and glasses; API in private preview; Meta itself acknowledged gaps in "coding workflows and complex multistep agentic tasks." **Vibes** (Meta AI's AI-video feed) still uses third-party models. Aggregators also list a **Muse Wonder** at $4/$20 and **Muse Spark 1.3** at $1.25/$4.25 **[unverified — aggregator only]**. The one Meta model that matters for this stack is **Muse Glimmer** (10 Aug 2026), a 30B Apache-2.0 open-weight multimodal model built for local coding agents on Ollama/MLX. Note: Meta's $2B Manus acquisition was blocked by Chinese regulators and unwound (Meta cut ties 15 Jun 2026). [Meta newsroom](https://about.fb.com/news/2026/04/introducing-muse-spark-meta-superintelligence-labs/), [CNBC](https://www.cnbc.com/2026/04/08/meta-debuts-first-major-ai-model-since-14-billion-deal-to-bring-in-alexandr-wang.html), [Built In](https://builtin.com/articles/meta-muse-spark-ai-model), [Ollama Muse Glimmer](https://ollama.com/blog/muse-glimmer), [TechCrunch on Manus](https://techcrunch.com/2026/10/08/chinas-manus-raises-over-500m-in-first-funding-round-since-split-with-meta/)
- **Best used for:** consumer reach (if you publish to Instagram/WhatsApp audiences) and Glimmer as a free local coder. Not a CEO-grade model.

### 3.4 xAI Grok
Grok 4.7 (21 Sep 2026) is the flagship: 500K context, $2/$6 (doubles above 200K). Grok Build 0.1 $1/$2 is a coding model; **Grok Bot** (beta since 11 Aug 2026) is an always-on cloud agent bundled with X Premium/Super/Ultra. Grok 5 is unreleased with no date. [xAI models](https://docs.x.ai/docs/models), [geotoolbox tracker](https://geotoolbox.ai/blog/grok-5)
- **Best used for:** real-time X/Twitter data, cheap long-context reasoning, contrarian second opinions.

### 3.5 Perplexity and Manus
- **Perplexity Computer** (25 Feb 2026): cloud agent that decomposes goals and routes subtasks across ~19 models in isolated sandboxes; Personal Computer runs on a Mac mini; Max $200/mo, limited Pro access. Best for research-heavy deliverables and as a benchmark for "multi-model routing" done well. [buildfastwithai](https://www.buildfastwithai.com/blogs/what-is-perplexity-computer), [PCWorld](https://www.pcworld.com/article/3071595/perplexitys-new-tool-deploys-teams-of-ai-agents.html)
- **Manus**: autonomous cloud agent (browser + terminal + FS), "My Computer" local app (Mar 2026), now independent again after the Meta deal collapsed; raised $500M+ on 8 Oct 2026; selling "Cue" (agents with phone numbers and budgeted wallets). Free tier; paid from ~$19/mo **[pricing unverified]**. Chinese-regulated ownership is a consideration for sensitive data. [TechCrunch](https://techcrunch.com/2026/10/08/chinas-manus-raises-over-500m-in-first-funding-round-since-split-with-meta/), [Sliq comparison](https://getsliq.com/blog/perplexity-computer-vs-manus-ai)

### 3.6 Open-weight models (hosted via API or self-hosted)
| Model | License | Size | API price (in/out) | Note |
|---|---|---|---|---|
| DeepSeek V4 Pro / V4.1 Flash (Sep 10, 1017 update) | MIT | 1.6T/49B active; Flash ~552B | $1.32/$3.96; $0.30/$1.20 (off-peak cheaper) | Top open model on SWE-bench Verified (~80%) per secondary sources |
| Kimi K3 (16 Jul; weights 27 Jul 2026) | Custom (>$20M revenue needs contract) | 2.8T / 104B active, 1M ctx | $3/$15 | Needs ≥64 accelerators; K2.6 (Modified MIT) $0.95/$4 |
| Qwen3.8-27B / Qwen3.8-2.4T-A95B (Aug 2026) | Apache-2.0 / custom | 27B dense; 2.4T MoE | Qwen3.7 Flash $0.03/$0.13; 3.5 Plus $0.40/$2.40 | 27B is the best self-hostable all-rounder |
| Llama 4 (Apr 2025) | Llama Community | — | — | Trails on coding/reasoning; 10M context Scout niche |
| gpt-oss-20b/120b | Apache-2.0 | — | — | Solid 16 GB local option |

Sources: [benchlm pricing table](https://benchlm.ai/llm-pricing), [SiliconFlow on V4.1 Flash](https://www.siliconflow.com/blog/deepseek-v4-1-flash-api-migration), [Kimi K3 HF blog](https://huggingface.co/blog/ResterChed/kimi-k3-model-overview-mxfp4-quantization-open-wei), [the-decoder Qwen3.8](https://the-decoder.com/alibabas-qwen-team-releases-qwen-3-8-models-with-open-weights-under-the-apache-2-0-license/), [codersera comparison](https://codersera.com/blog/best-open-source-llm-2026-llama-4-qwen-3-5-deepseek-v4-gemma-4-mistral/). Benchmark numbers are self-reported or from aggregators **[treat as approximate]**.

### 3.7 Which model for which job (rough list cost per 1M in/out)

| Job | First choice | Alternative | Why |
|---|---|---|---|
| CEO/planning, hard decisions, final review | Claude Fable 5.1 ($10/$50) | Opus 5.5 at `xhigh` effort | Longest-horizon reasoning; use sparingly |
| Day-to-day orchestration, agentic coding, computer use | Claude Opus 5.5 ($4/$20) | GPT-6.1 Sol ($2/$10), Gemini 4 Argon ($2/$10 intro) | Leads Terminal-Bench 4.0 / OSWorld per Anthropic; default in Claude Code |
| Worker subagents (tests, docs, research legs) | Claude Sonnet 5.5 ($2/$10) | Gemini 3.8 Flash ($0.75/$3.75) | Cost/quality balance; Anthropic recommends Sonnet for teammates |
| Classification, routing, extraction, summarizing inbox | Claude Haiku 5.5 ($0.10/$0.50) | GPT-6 Luna ($0.10/$0.50), DeepSeek V4.1 Flash ($0.30/$1.20) | Pennies; keep prompts <100K tokens for Haiku's low tier |
| Independent code review / red team | GPT-6.1 Sol ($2/$10) | Grok 4.7 ($2/$6) | Different training lineage catches different bugs |
| Video/audio understanding, voice agent | Gemini 3.8 Flash / 3.8 Live ($0.75/$3.75–4.50) | — | Native multimodal, free dev tier |
| Image generation for marketing | Gemini Nano Banana 2.1 | Meta AI/Vibes (consumer) | — |
| Private/offline triage on the Mac mini | Qwen3.6-27B or Muse Glimmer 30B (free) | Qwen3.8-27B (48 GB+) | No data leaves the machine |
| Bulk cheap text at scale | DeepSeek V4.1 Flash ($0.30/$1.20) | Qwen3.7 Flash ($0.03/$0.13) | Cheapest hosted quality; check data-residency needs |
| Real-time social/X signal | Grok 4.7 | Perplexity API | Live X data |

Prices: [Anthropic](https://platform.claude.com/docs/en/about-claude/pricing), [OpenAI](https://developers.openai.com/api/docs/pricing), [Google](https://ai.google.dev/gemini-api/docs/pricing), [xAI](https://docs.x.ai/docs/models), [benchlm aggregate](https://benchlm.ai/llm-pricing).

---

## 4. Multi-agent orchestration patterns that actually work

### 4.1 Patterns
1. **Orchestrator–worker (lead + fresh-context subagents).** Anthropic's own research system: a lead plans, spawns 3–5 subagents in parallel with explicit objective/output format/tool guidance/boundaries, each returns condensed findings; subagents write artifacts to the filesystem and pass references, not blobs. Multi-agent Opus-lead/Sonnet-workers beat single Opus by 90% on their research eval — but at ~15x chat token cost. Works for breadth-first, parallelizable work; poorly for tightly coupled coding. [Anthropic multi-agent research system](https://www.anthropic.com/engineering/multi-agent-research-system)
2. **Role-based "org chart" (CEO/COO/CMO…).** Implement roles as `.claude/agents/*.md` subagent definitions with their own `memory: project`, tools allowlist, model, and `effort`. The CEO session (Opus/Fable) is the only one that talks to you and writes to `docs/decisions/`; functional roles run as subagents or scheduled tasks. A solo-founder guide suggests 8–15 roles across 3–4 "circles" — more than that is overhead. Project Vend is the cautionary tale: a Claude left to run a shop autonomously drifted badly; keep humans at the money and identity boundaries. [nestr.io guide](https://nestr.io/blog/build-ai-agent-team-solo-founder), [TechCrunch on Project Vend](https://techcrunch.com/2025/06/28/anthropics-claude-ai-became-a-terrible-business-owner-in-experiment-that-got-weird), [Sub-agents](https://code.claude.com/docs/en/sub-agents)
3. **Shared memory via git.** Every role writes to the same repo on its own branch/worktree; the CEO merges. Claude Code gives you worktrees (`claude --worktree`, `isolation: worktree`), `claude/`-prefixed branches for cloud runs, and GitHub branch protection as the enforcement layer. Single-writer rule per file region avoids the "lost update" failure. [Scheduled tasks](https://code.claude.com/docs/en/routines), [Galileo failure modes](https://galileo.ai/blog/why-multi-agent-systems-fail)
4. **Event-driven instead of polling.** Cloud task API triggers (POST + bearer token), GitHub-event triggers, and Channels webhooks replace cron loops; Claude Code's `Monitor` tool streams a background script's output instead of re-prompting on a timer. [Scheduled tasks](https://code.claude.com/docs/en/routines), [/loop docs](https://code.claude.com/docs/en/scheduled-tasks)
5. **Frameworks, when you need them:**
   - **Claude Agent SDK** — same harness as Claude Code, deepest MCP integration, Claude-only; lighter on multi-agent orchestration primitives. [SDK overview](https://code.claude.com/docs/en/agent-sdk/overview)
   - **LangGraph** — strongest persistence/checkpointing and lowest token overhead in comparisons; best for production state machines. **CrewAI** — fastest role-based prototype (~3x LangGraph's tokens in one benchmark). **OpenAI Agents SDK** — simplest handoffs, works with non-OpenAI models. **Google ADK / Antigravity SDK** — if you're Gemini-centric. Combine: LangGraph outer graph, Claude SDK inside nodes. [requesty comparison](https://www.requesty.ai/blog/best-ai-agent-sdks-compared-2026-langchain-crewai-openai-anthropic-google), [morphllm](https://www.morphllm.com/ai-agent-framework), [the-agent-report](https://the-agent-report.com/2026/07/ai-agent-frameworks-comparison-2026-langgraph-crewai-autogen/)
   - **Managed Agents** — if you'd rather not run infra: sessions, memory stores, outcomes, budgets, scheduled deployments, webhooks. [Overview](https://platform.claude.com/docs/en/managed-agents/overview)
   - **Glue:** n8n (self-hostable, per-execution pricing, native instance-level MCP server since Apr 2026) for SaaS plumbing; Zapier MCP exposes 30,000+ actions as tools; Make is the least mature on MCP. [dev.to comparison](https://dev.to/shaam_ai/ai-connect-tools-compared-2026-n8n-wins-hk9), [cowork.ink comparison](http://cowork.ink/blog/n8n-vs-zapier-vs-make-ai/)

### 4.2 Known failure modes and mitigations

| Failure | What it looks like | Mitigation |
|---|---|---|
| Runaway cost | Nested fan-out where no layer sees total spend; agent-to-agent loops | Per-run `max_budget_usd` (SDK), Managed Agents per-run `budget`, Projects' 200-threads/day cap, `CLAUDE_CODE_MAX_CONCURRENT_SUBAGENTS`, spawn-depth 1–2, usage credits with a monthly spend limit, `/usage` attribution; Claude Code throttles cross-session message loops automatically |
| Context rot | Accuracy drops as context grows; distractors cause hallucination; compaction drops a standing instruction (the Gmail-deletion incident) | Fresh-context subagents returning 1–2K summaries; `/clear` between tasks; `autoCompactWindow`; keep must-never-drop rules in CLAUDE.md/hooks, not chat; Chroma's finding that ~300-token focused prompts beat 113K dumps |
| Agents overwriting each other's memory | Lost updates in shared MEMORY.md or files | One owner per file/region; per-role `agent-memory` dirs; worktrees + PRs; Managed Agents' Dreams produce a *new* store instead of mutating the input; file-locked task claiming in Agent Teams |
| Cascading errors / silent failure | One bad output poisons downstream agents; a "green" run that did nothing | Schema-validated handoffs; critic/verifier subagent; `TaskCompleted` hooks that exit 2 to reject; read the transcript — Claude's docs warn a green status "does not mean the work your prompt describes succeeded" |
| Prompt injection via inputs | Slack history, fire payloads, web pages steer the agent | Fire payloads arrive as untrusted data; messages between sessions can't grant consent; auto-mode classifier screens inter-agent messages; Opus 5.5 is more injection-resistant; channels use sender allowlists |
| Over-engineering | 15 agents for a 1-agent job | Start with one session + subagents; add teams only for parallel exploration; "three focused teammates often outperform five scattered ones" |

Sources: [Anthropic multi-agent system](https://www.anthropic.com/engineering/multi-agent-research-system), [Context rot](https://www.trychroma.com/research/context-rot), [Agent teams](https://code.claude.com/docs/en/agent-teams), [Costs](https://code.claude.com/docs/en/costs), [Scheduled tasks](https://code.claude.com/docs/en/routines), [dev.to failure modes](https://dev.to/gabrielanhaia/the-5-failure-modes-of-multi-agent-systems-nobody-warns-you-about-2fml), [Splunk coordination strategies](https://www.splunk.com/en_us/blog/artificial-intelligence/multi-agent-coordination-strategies.html), [arXiv: silent failure / entropy](https://arxiv.org/pdf/2606.08162), [BetterClaw incident list](https://www.betterclaw.io/blog/openclaw-security-2026)

---

## 5. Keeping the AI "upgraded": a 45-minute weekly routine

**Automate it.** Create one cloud scheduled task (Monday 07:07, Haiku or Sonnet) with the connectors it needs that: (1) fetches the Claude Code changelog, Anthropic news, OpenAI changelog, Gemini API changelog, xAI models page and Ollama blog; (2) diffs against last week's `docs/upgrades/last-seen.md` in the company repo; (3) opens a PR titled "Weekly upgrade digest" with a ranked list of changes that affect `CLAUDE.md`, model aliases, pricing assumptions, or installed plugins. You review the PR; merging it is the "upgrade."

**Your manual 45 minutes:**
1. Read the digest PR; update model IDs/prices in `CLAUDE.md` and subagent frontmatter (10 min).
2. `claude update`; `/plugin marketplace update`; `/skill-doctor`; `/doctor prompt-audit` to find contradictory instructions (10 min).
3. `/usage` (week view) — apply the "f to fix" recommendations; check usage-credit spend (5 min).
4. Skim auto memory (`/memory`) and `agent-memory/` dirs for stale or wrong facts; prune (10 min).
5. On the Mac mini: `openclaw doctor --fix` / `brew upgrade ollama` / `ollama pull` for the one or two local models you actually use; rotate any credential older than 90 days (10 min).

**Sources to monitor (primary first):**
- Anthropic: [Claude Code changelog](https://code.claude.com/docs/en/changelog) (RSS via GitHub releases of `anthropics/claude-code`), [anthropic.com/news](https://www.anthropic.com/news), [Models overview](https://platform.claude.com/docs/en/about-claude/models/overview), [Agent SDK changelog mirror](https://www.gradually.ai/en/changelogs/claude-agent-sdk/), [claude-plugins-official](https://github.com/anthropics/claude-plugins-official), [Skills Marketplace](https://claude.com/marketplace), [Anthropic engineering blog](https://www.anthropic.com/engineering).
- OpenAI: [ChatGPT & Codex changelog](https://learn.chatgpt.com/docs/changelog), [API pricing](https://developers.openai.com/api/docs/pricing), openai.com/news RSS.
- Google: [Gemini API changelog](https://ai.google.dev/gemini-api/docs/changelog) (Releasebot mirror [here](https://releasebot.io/updates/google/gemini-api)), [Google developers blog](https://blog.google/innovation-and-ai/technology/developers-tools/).
- Others: [xAI models](https://docs.x.ai/docs/models), [Ollama blog](https://ollama.com/blog), Hugging Face trending, [OpenClaw releases](https://github.com/openclaw/openclaw/releases) and the [OpenClawCVEs tracker](https://github.com/jgamblin/OpenClawCVEs).
- Aggregators/newsletters: [Releasebot (Anthropic)](https://releasebot.io/updates/anthropic), [aichangelog.dev](https://aichangelog.dev/), [Latent Space](https://www.latent.space/), Simon Willison's blog ([simonwillison.net](https://simonwillison.net/), the most reliable single human filter on model releases), [daily.dev's guide to tracking releases](https://daily.dev/blog/track-new-ai-model-releases-without-refreshing-x/), [benchlm pricing trends](https://benchlm.ai/llm-pricing-trends), MCP registry updates via [claudemarketplace.net](https://www.claudemarketplace.net/).

---

## 6. Things I could not verify (act on these cautiously)
- Exact GA date of Claude in Chrome (sources say 26 Aug 2026 or "since July").
- Whether MLX is now Ollama's default engine on Apple Silicon.
- Meta "Muse Wonder" and "Muse Spark 1.3" API pricing (aggregator only).
- Manus current pricing and "My Computer" app status post-Meta split.
- Hermes Agent direct Anthropic provider support.
- OpenClaw's current latest version (newest confirmed in sources: 2026.8.1 security fixes; 2026.7.1 in NemoClaw).
- Claude Max weekly token ceilings (Anthropic publishes multipliers, not tokens).
- Third-party SWE-bench numbers for open-weight models (self-reported).
- The "~15x tokens" multi-agent figure is from Anthropic's June 2025 research system; current models and caching change the ratio.

---

## Appendix: minimal company-repo layout

```
company/
├── CLAUDE.md                 # constitution: mission, boundaries, "never do" list, model policy (<200 lines)
├── .claude/
│   ├── rules/                # finance.md, marketing.md, security.md (path-scoped where possible)
│   ├── skills/               # weekly-digest/, invoice-run/, customer-reply/ (SKILL.md each)
│   ├── agents/               # ceo.md, coo.md, cmo.md, reviewer.md  (memory: project, model, tools, effort)
│   ├── agent-memory/         # versioned learnings per role
│   ├── hooks/                # PreToolUse guards (no rm -rf, no payments without approval)
│   ├── loop.md               # default maintenance loop for the resident session
│   └── settings.json         # autoMemoryDirectory -> ./.claude/auto-memory, deny rules, env caps
├── docs/
│   ├── decisions/            # ADR-style log the CEO appends to
│   ├── okrs.md
│   ├── runs/                 # one markdown per scheduled run (what happened, cost)
│   └── upgrades/last-seen.md
└── .mcp.json                 # project-scoped MCP servers for cloud runs
```
