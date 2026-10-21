# The Owner's Playbook: Running a Company with an AI CEO

*Prepared October 2026 for a non-technical Owner who runs the company through Claude (as CEO) and a team of Claude subagents, from claude.ai/code cloud sessions and a Mac mini. Every factual claim about Claude features links to Anthropic's own documentation; research claims link to the primary paper or post.*

---

## Part 1. The 10 habits of people who get the most out of agentic AI

The evidence base here is Anthropic's internal study of its own engineers ([How AI is transforming work at Anthropic](https://www.anthropic.com/research/how-ai-is-transforming-work-at-anthropic), Dec 2025: 132 surveyed, 53 interviewed, ~200,000 Claude Code transcripts), the Anthropic Economic Index ([Impact on software development](https://www.anthropic.com/research/impact-software-development), [January 2026 report](https://www.anthropic.com/research/anthropic-economic-index-january-2026-report), [June 2026 "Cadences" report](https://www.anthropic.com/research/economic-index-june-2026-report)), Anthropic's [Claude Code best practices](https://code.claude.com/docs/en/best-practices), and practitioner writing by [Ethan Mollick](https://www.oneusefulthing.org/p/management-as-ai-superpower) and [Simon Willison](https://simonwillison.net/2025/Jun/16/the-lethal-trifecta/).

**1. Brief like a manager, not like a searcher.** Mollick's delegation checklist is the single best template: state the goal and why it matters, the limits of authority you are handing over, what "done" looks like, the specific deliverables, interim checkpoints, and what the agent must verify before reporting back. His line: "What's scarce is knowing what to ask for." Anthropic's own docs say the same thing in engineering terms: "The more precise your instructions, the fewer corrections you'll need," and vague prompts like "improve this" trigger expensive, broad exploration ([best practices](https://code.claude.com/docs/en/best-practices); [costs](https://code.claude.com/docs/en/costs#write-specific-prompts)). For your CEO, the brief is: objective, budget, deadline, what you will not accept, how to prove it worked.

**2. Always give the AI a way to check its own work.** This is Anthropic's top-ranked practice: "Give Claude a check it can run... It's the difference between a session you watch and one you walk away from." Without a check, "looks done" is the only signal and *you* become the verification loop. In business terms: a finished invoice run must reconcile to a total; a drafted email campaign must pass a checklist; a report must cite the data file it came from. Ask for evidence (the number it checked, the command it ran) rather than assertions.

**3. Delegate the verifiable, collaborate on the judgmental.** Anthropic's engineers delegate work that is easily verifiable, low-stakes, repetitive, well-scoped, and decoupled; they keep high-level design, strategy, and decisions needing organizational context or "taste." Over half said they could *fully* delegate only 0–20% of their work, and the boundary is "a moving target" as models improve. The Economic Index confirms the split: 79% of Claude Code conversations are automation-style versus 49% on Claude.ai ([Impact on software development](https://www.anthropic.com/research/impact-software-development)), and the January 2026 report found Claude.ai's iterative, multi-turn use had a 67% success rate versus 49% for directive API use, "where users clarify and correct course" ([Jan 2026 report](https://www.anthropic.com/research/anthropic-economic-index-january-2026-report)). The rule: delegate fully when you can check the result in under a minute; collaborate turn-by-turn when the task needs your judgment.

**4. Start small, expand trust on evidence.** Anthropic's engineers describe trust building "gradually, starting with simple tasks and moving to more complex ones," and the Economic Index shows success falls as complexity rises (about 60% for sub-hour tasks down to about 45% for 5+ hour tasks on the API). Give your CEO one new autonomous responsibility per week, not ten.

**5. Review for plausible errors, not typos.** Mollick: use domain expertise "to catch plausible-looking errors, which are the hardest failures to spot." An Anthropic security engineer put it the same way: a plausible proposal can still be dangerous. Anthropic's docs call this "the trust-then-verify gap" and the fix is blunt: "If you can't verify it, don't ship it." Your review should ask: what would be wrong here if this were wrong? Check that one thing.

**6. Correct early, and after two failed corrections, start over.** From the docs: "If you've corrected Claude more than twice on the same issue in one session, the context is cluttered with failed approaches. Run `/clear` and start fresh with a more specific prompt that incorporates what you learned." Corrections you keep repeating are not feedback; they are missing rules (see Part 4).

**7. Keep memory short and specific.** CLAUDE.md is "context, not enforced configuration." Anthropic's guidance: target under 200 lines; for each line ask "Would removing this cause Claude to make mistakes?" and cut it if not, because "bloated CLAUDE.md files cause Claude to ignore your actual instructions" ([memory](https://code.claude.com/docs/en/memory); [best practices](https://code.claude.com/docs/en/best-practices)). Procedures go in skills (loaded on demand), hard rules go in hooks (enforced by the harness), only always-true facts go in CLAUDE.md.

**8. Stop babysitting by closing the loop with tools, not attention.** Anthropic's docs describe the ladder: verification in the prompt (works today), a `/goal` condition re-checked after every turn, a Stop hook that blocks a session from ending until a script passes, and an adversarial review by a fresh subagent that "sees only the diff and the criteria you give it." Scheduled tasks run unattended in the cloud ([web scheduled tasks](https://code.claude.com/docs/en/web-scheduled-tasks)). The goal is that you read evidence, not watch work.

**9. Use fresh context for review.** "A fresh context improves code review since Claude won't be biased toward code it just wrote." Have one session write, another review. In your company: the CEO drafts the weekly plan; a separate reviewer subagent checks it against the 90-day plan and flags gaps, not style preferences.

**10. Keep your own skills sharp, and measure.** Anthropic's engineers worried about "the paradox of supervision": supervising Claude requires skills that overuse may erode. Some deliberately work without AI sometimes. The June 2026 Economic Index survey (~9,700 respondents) found heavier delegators report more learning and more optimism about pay and job security, but the authors note self-assessment "cannot rule out skill erosion." The Owner's defense: learn the fundamentals in Part 2, and track the numbers in Part 4 so you know whether delegation is actually working.

---

## Part 2. The 8-week learning curriculum (30–45 minutes a day)

All Anthropic Academy courses are free, self-paced, and live at [academy.claude.com](https://academy.claude.com/) (anthropic.com/learn redirects there). Course lengths are from the catalog page. Split each course across several days.

### Week 1 – Fluency: what AI can and cannot do
- **Course:** [Claude 101](https://academy.claude.com/courses/claude-101) (2.5 hr). *Unlocks:* confident use of chat, Projects, connectors, memory.
- **Course:** [AI capabilities and limitations](https://academy.claude.com/courses/ai-capabilities-and-limitations) (3.5 hr, start it; finish in week 2). *Unlocks:* knowing when the AI is likely to be wrong.
- **Read:** [How AI is transforming work at Anthropic](https://www.anthropic.com/research/how-ai-is-transforming-work-at-anthropic). *Unlocks:* a realistic model of delegation (0–20% fully delegable today, expanding).
- **Do:** Write the first 20-line CLAUDE.md for the company: what the business is, who the customer is, what you will never do without the Owner.

### Week 2 – Prompting fundamentals
- **Course:** finish AI capabilities and limitations; start [AI Fluency: Framework and foundations](https://academy.claude.com/courses/ai-fluency-framework-foundations) (4 hr) and [AI Fluency for small businesses](https://academy.claude.com/courses/ai-fluency-for-small-businesses).
- **Read:** [Prompting best practices](https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/claude-prompting-best-practices) (the living reference for clarity, examples, XML structure, role prompts, chaining) and the [prompt engineering overview](https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/overview). The [interactive tutorial on GitHub](https://github.com/anthropics/prompt-eng-interactive-tutorial) is optional.
- **Read:** [Mollick, "Management as AI superpower"](https://www.oneusefulthing.org/p/management-as-ai-superpower). *Unlocks:* the delegation brief format you will use every day.
- **Do:** Rewrite three recent requests to the CEO using goal / constraints / definition of done / verification.

### Week 3 – Claude Code: the operating surface
- **Course:** [Claude Code 101](https://academy.claude.com/courses/claude-code-101) (1.5 hr) and [Claude Code in action](https://academy.claude.com/courses/claude-code-in-action) (1 hr). *Unlocks:* sessions, permission modes, `/clear`, `/compact`, plan mode.
- **Read:** [Best practices](https://code.claude.com/docs/en/best-practices) (the single most useful page in this playbook) and [How Claude remembers your project](https://code.claude.com/docs/en/memory).
- **Do:** Run `/init` on the company repo, read what it wrote, prune it.

### Week 4 – Cowork, scheduled tasks, and the Mac mini
- **Course:** [Introduction to Claude Cowork](https://academy.claude.com/courses/introduction-to-claude-cowork) (2.5 hr). *Unlocks:* non-coding desktop work: files, browser, documents.
- **Read:** [Web scheduled tasks](https://code.claude.com/docs/en/web-scheduled-tasks), [Desktop scheduled tasks](https://code.claude.com/docs/en/desktop-scheduled-tasks), [Cowork scheduled tasks](https://support.claude.com/en/articles/13854387).
- **Do:** Create the Monday brief as a scheduled task (Part 3 and Part 4).

### Week 5 – Agents, skills, MCP
- **Course:** [Introduction to subagents](https://academy.claude.com/courses/introduction-to-subagents) (45 min), [Introduction to agent skills](https://academy.claude.com/courses/introduction-to-agent-skills) (1 hr), [Introduction to Model Context Protocol](https://academy.claude.com/courses/introduction-to-model-context-protocol) (1 hr). *Unlocks:* understanding how your "team" is built: a subagent is a role with its own context and tools; a skill is a documented procedure; MCP is how Claude reaches your tools.
- **Read:** [Building effective agents](https://www.anthropic.com/research/building-effective-agents) (start simple; add autonomy only when it clearly improves outcomes; checkpoints and stopping conditions), [Skills](https://code.claude.com/docs/en/skills), [Subagents](https://code.claude.com/docs/en/sub-agents), [modelcontextprotocol.io](https://modelcontextprotocol.io).
- **Do:** Build your first custom skill (Part 3).

### Week 6 – Business finance literacy
- **Free:** [Khan Academy: Finance and capital markets](https://www.khanacademy.org/economics-finance-domain) (pick the accounting and financial statements units) and the [SBA Learning Center](https://www.sba.gov/sba-learning-platform) courses on cash flow and pricing.
- **Book:** *Financial Intelligence for Entrepreneurs* (Berman and Knight) or *Profit First* (Michalowicz) if you want a cash-first system.
- **Unlocks:** reading the P&L, balance sheet and cash flow your CEO produces, and catching the plausible-looking error (habit 5). You cannot delegate what you cannot verify.
- **Do:** Have the CEO produce a 30/60/90 day cash forecast and explain every assumption to you.

### Week 7 – Sales for people who hate selling
- **Free:** [HubSpot Academy, Inbound Sales](https://academy.hubspot.com) certification (free) and [Y Combinator Startup School](https://www.startupschool.org) talks on talking to users.
- **Books:** *The Mom Test* (Fitzpatrick) for customer conversations; *To Sell Is Human* (Pink) for reframing selling as helping. Optional: *SPIN Selling* (Rackham) for structured discovery.
- **Unlocks:** the CEO can draft outreach and triage leads, but the first ten customer conversations are yours. These books make them bearable.
- **Course:** [Building effective human-agent teams](https://academy.claude.com/courses/building-effective-human-agent-teams) (45 min, beta).

### Week 8 – Operating at scale, security, upgrade loop
- **Read:** [Simon Willison, "The lethal trifecta"](https://simonwillison.net/2025/Jun/16/the-lethal-trifecta/), [Claude for Chrome security](https://claude.com/blog/claude-for-chrome), [Manage costs](https://code.claude.com/docs/en/costs), [Projects on claude.ai/code](https://code.claude.com/docs/en/claude-projects), [Channels](https://code.claude.com/docs/en/channels).
- **Book:** *Co-Intelligence* (Mollick), the best general book on working with AI.
- **Do:** Run the first weekly review and the first 30-minute model evaluation (Part 5).

### The best 10 free resources (bookmark these)
1. [Claude Academy](https://academy.claude.com/) – all 27 courses, free.
2. [Claude Code docs: best practices](https://code.claude.com/docs/en/best-practices).
3. [Prompting best practices](https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/claude-prompting-best-practices).
4. [Anthropic Economic Index](https://www.anthropic.com/economic-index) – evidence on what delegation looks like.
5. [One Useful Thing](https://www.oneusefulthing.org/) – Mollick's newsletter.
6. [Simon Willison's weblog](https://simonwillison.net/) – security and agent practice.
7. [Claude Code changelog](https://code.claude.com/docs/en/changelog) – what shipped this week.
8. [Claude Help Center](https://support.claude.com/) – plans, Cowork, skills, connectors.
9. [Khan Academy finance](https://www.khanacademy.org/economics-finance-domain) and [SBA Learning Center](https://www.sba.gov/sba-learning-platform).
10. [HubSpot Academy](https://academy.hubspot.com) and [YC Startup School](https://www.startupschool.org).

---

## Part 3. The feature checklist to unlock now

### 3.1 Which plan you need ([claude.com/pricing](https://claude.com/pricing))
| Need | Minimum plan | Notes |
|---|---|---|
| Projects | Free (up to 5), unlimited on paid | |
| Connectors | All plans | Admin controls on Team/Enterprise |
| Claude Code (terminal, desktop, cloud) | Pro | Max 5x/20x for heavy agent use |
| Claude Cowork | Pro, Max (desktop: all paid; web/mobile: Pro, Max, Team) | Pricing page says Cowork is "now just Claude" and rolling out |
| Claude in Chrome | Any paid plan | Free plan excluded ([claude.com/chrome](https://claude.com/chrome)) |
| Cloud scheduled tasks (Claude Code) | Pro, Max, Team, Enterprise | [docs](https://code.claude.com/docs/en/web-scheduled-tasks) |
| Cowork scheduled tasks | All paid plans | [help article](https://support.claude.com/en/articles/13854387) |
| Claude Code Projects (parallel cloud threads) | Pro, Max (public beta, gradual rollout) | Not yet on Team/Enterprise ([docs](https://code.claude.com/docs/en/claude-projects)) |
| Usage credits (keep working past limits) | Pro, Max; admin-enabled on Team | [help](https://support.claude.com/en/articles/12429409-extra-usage-for-paid-claude-plans) |

**Recommendation:** Max (5x) for the Owner account running the CEO. An AI-operated business runs scheduled tasks and subagents all day; each subagent "makes its own API requests, which count toward your usage limits" ([subagents](https://code.claude.com/docs/en/sub-agents)). Turn on usage credits with a monthly spend limit at [claude.ai/settings/usage](https://claude.ai/settings/usage) so a runaway task hits a ceiling instead of a surprise.

### 3.2 Connectors to authorize first (at [claude.ai/customize/connectors](https://claude.ai/customize/connectors))
Order by what the CEO needs to see before it can act:
1. **Google Workspace or Microsoft 365** (Gmail/Outlook, Calendar, Drive): the inbox and the files are the company's nervous system.
2. **Accounting** (QuickBooks, Xero): the CEO cannot run the company without the numbers.
3. **Payments** (Stripe, Square, Shopify as applicable): revenue in real time.
4. **CRM** (HubSpot): pipeline and customer history.
5. **Slack** (if you have one): where approvals and briefs get posted.
6. **GitHub**: required for cloud scheduled tasks (each run clones a repository); the company "repo" is where CLAUDE.md, skills and decision logs live.
7. **Canva** for marketing assets; **Zapier** for anything without a connector (the [Marketplace](https://claude.com/marketplace) lists over 2,000 connectors and plugins).

Rule from the scheduled-tasks docs: "All of your connected MCP connectors are included by default. Remove any the task doesn't need: Claude can use every tool from an included connector, including writes, without asking for permission during a run." Scope every task to the connectors it needs.

### 3.3 Mac mini setup (one evening)
1. Install **Claude Desktop** for macOS ([deploy guide](https://support.claude.com/en/articles/12611117-deploy-claude-desktop-for-macos)); Cowork installs with it and the universal build runs on Intel and Apple silicon. Sign in with the paid account. Cowork desktop gives local file access, browser use and computer use ([Cowork help](https://support.claude.com/en/articles/13345190)).
2. Install **Claude Code**: open Terminal and run `curl -fsSL https://claude.ai/install.sh | bash`, then `claude --version` and `claude` to log in with the claude.ai account ([quickstart](https://code.claude.com/docs/en/quickstart)). Native installs auto-update.
3. Create the company folder as a git repository, add CLAUDE.md, `.claude/skills/`, `.claude/agents/`, and a `decisions/` folder. Push it to a private GitHub repo so cloud scheduled tasks can clone it.
4. In Claude Desktop: Settings > This computer > System > **Keep computer awake**, because desktop scheduled tasks "only run while the desktop app is running and your computer is awake" ([desktop scheduled tasks](https://code.claude.com/docs/en/desktop-scheduled-tasks)). Use the Mac for local-file tasks; use cloud tasks for anything that must run reliably.
5. Install the **Claude in Chrome** extension from the Chrome Web Store on the Mac mini.
6. Set up **Remote Control** so you can steer a Mac session from your phone: the session "keeps running locally the entire time" and you can send photos and messages from the Claude app ([remote control](https://code.claude.com/docs/en/remote-control)).
7. Optional: a **Channel** (Telegram, Discord or iMessage) so the CEO can message you and you can reply from your phone: `/plugin install telegram@claude-plugins-official`, then `claude --channels plugin:telegram@claude-plugins-official`, pair, and set the access policy to allowlist ([channels](https://code.claude.com/docs/en/channels)). Research preview; Pro/Max users can opt in per session.

### 3.4 How scheduled tasks and notifications work
Three kinds, compared in the docs ([compare scheduling options](https://code.claude.com/docs/en/desktop-scheduled-tasks#compare-scheduling-options)):
- **Cloud scheduled tasks** (create at [claude.ai/code/routines](https://claude.ai/code/routines) or `/schedule` in the CLI): run on Anthropic infrastructure with your laptop closed; triggers are schedule, API call, or GitHub event; minimum interval one hour; each run is a full cloud session you can open and read. "The prompt is the most important part: the task runs autonomously, so the prompt must be self-contained and explicit about what to do and what success looks like." A green status "does not mean the work your prompt describes succeeded. Open the run to read the transcript." Limits: 100 scheduled runs per hour per account; runs draw down subscription usage.
- **Desktop scheduled tasks**: run on the Mac with local files; minimum interval one minute; missed runs get one catch-up on wake. Set permissions per task and click **Run now** once to pre-approve tools so future runs don't stall.
- **Cowork scheduled tasks**: described in plain language in any conversation; each run is its own Cowork session reviewed under **Scheduled** in the sidebar ([help](https://support.claude.com/en/articles/13854387)).

**Notifications:** Anthropic's docs do not describe push notifications for scheduled-task completion. The reliable patterns are: have the task post its result to Slack or email through a connector; use a Channel for two-way chat on your phone; or check the **Scheduled** page. Write the "post the summary to Slack #brief" step into every task prompt.

### 3.5 The marketplace and plugins
- Browse [claude.com/marketplace](https://claude.com/marketplace) (connectors, plugins, partners). In Claude Code run `/plugin` to open the **Discover** tab; Anthropic's official marketplace (`claude-plugins-official`) is registered automatically ([install plugins](https://code.claude.com/docs/en/plugins/install)).
- Review **Will install** and **Context cost** before installing; plugins can run hooks and MCP servers. Prefer user scope for personal tools, project scope for company tools.
- Plugins you enable on claude.ai sync to Claude Code and Cowork automatically; the reverse is not true.
- Already available in this workspace: a `small-business` plugin with skills such as business-pulse, cash-flow-snapshot, invoice-chase, crm-autopilot, inbox-manager, build-agent and build-connector. Start there before building anything.

### 3.6 Build a custom skill (your first one this week)
A skill is a folder with a `SKILL.md` file: YAML frontmatter (`name`, `description` up to 200 characters, the field Claude uses to decide when to use it) and Markdown instructions ([create custom skills](https://support.claude.com/en/articles/12512198-how-to-create-custom-skills); [Claude Code skills](https://code.claude.com/docs/en/skills)).
1. Do the task once with Claude in a session, or describe it. The `small-business:build-agent` skill in this workspace is designed to turn a repeated task into a named skill.
2. Ask: "Turn what we just did into a skill called `weekly-invoice-chase` with an approval checkpoint before anything is sent."
3. Put it at `.claude/skills/weekly-invoice-chase/SKILL.md` in the company repo (shared with cloud sessions) or zip and upload at [claude.ai/customize/skills](https://claude.ai/customize/skills) (synced everywhere).
4. Keep SKILL.md under about 500 lines; put reference material in side files; add `disable-model-invocation: true` to any skill with side effects so only you can trigger it.
5. Test in a fresh session and compare results with the skill on and off.

### 3.7 Claude in Chrome for browser work
Use it for the long tail of tools without a connector: reading dashboards, filling supplier forms, gathering competitor pricing ([claude.com/chrome](https://claude.com/chrome)). Safety model: site-by-site permissions, confirmation before purchases and sensitive actions, blocked categories (financial services, adult, pirated content), and a safety check on each action in auto-approval mode. Anthropic's own red-team numbers: prompt-injection attacks succeeded 23.6% of the time without mitigations and 11.2% with them in autonomous mode, and 35.7% to 0% on a browser-specific challenge set ([Claude for Chrome](https://claude.com/blog/claude-for-chrome)). Their advice, which you should adopt as policy: start on trusted sites; do not use it for financial, legal or medical sites; do not store passwords in it.

### 3.8 Monitor usage and cost
- Plan usage: [claude.ai/settings/usage](https://claude.ai/settings/usage) (rolling five-hour window plus weekly limits; usage credits and a monthly spend limit live here).
- In Claude Code: `/usage` shows plan usage bars plus attribution by skill, subagent, plugin and MCP server, and recommendations (press `f` to apply fixes); `/context` shows what fills the window; `/insights` writes a report on friction points ([costs](https://code.claude.com/docs/en/costs)).
- Benchmarks: enterprise average is "around $13 per developer per active day and $150–250 per developer per month," and an agent team uses "approximately 7x more tokens than standard sessions." Treat those as the scale of what an always-on CEO costs.
- Cost levers from the docs: `/clear` between unrelated tasks, Sonnet or Haiku for subagents, keep CLAUDE.md under 200 lines, disable unused MCP servers, lower effort for simple tasks.

---

## Part 4. The operating rhythm and feedback protocol

### Daily (20 minutes, same time every morning)
1. **Read the brief** (5 min). A cloud scheduled task runs the `brief` skill at 06:07 (a few minutes past the hour, as the docs advise) and posts to Slack: yesterday's results against plan, today's three priorities, cash position, the short list of things only the Owner can do.
2. **Clear the approval queue** (10 min). Every action with money, customers, contracts or public content waits for a yes. Approve, reject, or reply "not this, because X" (see feedback protocol).
3. **One decision or one correction** (5 min). Either answer the one decision the CEO escalated, or convert one correction into a rule.

That is the whole day unless you choose more. The point of the rhythm is that the Owner's attention goes to decisions and verification, not supervision.

### Weekly (60 minutes, Sunday evening or Monday morning)
Run the `weekly` skill. It produces a scorecard against the 90-day plan, what worked, lessons, next week's single priority, and a memory update that gets committed. The Owner reviews, in this order:
- **Numbers first:** cash, revenue, pipeline, cost of AI usage from `/usage` and the usage page. Compare to last week.
- **Decision log:** every decision from the week, the option chosen, the reasoning, the expected outcome and the date to check it. The `decide` skill writes these to `decisions/YYYY-MM-DD-slug.md` in the company repo so they are versioned and searchable.
- **Autonomy review:** one task to promote from "needs approval" to "run autonomously" (if it passed verification four weeks in a row), and one to demote if it caused a correction.
- **Memory hygiene:** open `/memory`, read the auto-memory index, delete anything stale or contradictory, run `/doctor prompt-audit` to find conflicting instructions.
- **Upgrade scan:** run the `upgrade` skill (Part 5).

### The feedback protocol: how the AI improves from every interaction
Anthropic's memory docs say to add to CLAUDE.md when "Claude makes the same mistake a second time" or "you type the same correction or clarification into chat that you typed last session." The protocol:

**When output is wrong, say three things:** what is wrong, what right looks like, and whether this is a one-off or a rule. Example: "The invoice reminder is too aggressive for a customer who paid late once. Right looks like: friendly on first reminder, firm on third. Rule: always."

**Then route the correction:**
| Kind of correction | Where it lives | How to make it permanent |
|---|---|---|
| A fact or preference that applies everywhere ("we never discount below 15%") | CLAUDE.md in the company repo | Say "add this to CLAUDE.md." Keep under 200 lines. |
| A learned pattern Claude should remember ("the Owner reviews cash on Mondays") | Auto memory | Say "remember that..." and Claude writes it to `~/.claude/projects/<project>/memory/`. Check it with `/memory`. |
| A multi-step procedure that was done wrong | The relevant skill's SKILL.md | "Update the invoice-chase skill: step 3 should..." |
| Something that must never happen regardless of what Claude decides ("never send email without approval") | A hook | Ask Claude to "write a PreToolUse hook that blocks any Gmail send tool." Hooks are enforced by the harness; CLAUDE.md is advisory ([hooks guide](https://code.claude.com/docs/en/hooks-guide)). |
| A rule that only applies to one area (pricing files, customer emails) | `.claude/rules/<topic>.md` with a `paths` scope | Loads only when relevant, keeps CLAUDE.md small. |

**Close the loop:** after the rule is written, ask the CEO to restate it and to show the file diff. Next week, check whether the behavior actually changed; Anthropic's docs say to "treat CLAUDE.md like code: review it when things go wrong, prune it regularly, and test changes by observing whether Claude's behavior actually shifts."

**When output is good, say so briefly and name why.** Specific praise ("the brief led with cash, that is right") is cheaper than another correction later, and if you want it kept, say "remember that."

---

## Part 5. Keeping the AI upgraded continuously

### Sources to watch (15 minutes a week, delegated to the `upgrade` skill)
- [Anthropic news](https://www.anthropic.com/news) and the [Claude blog](https://claude.com/blog): model releases and product launches.
- [Claude Code changelog](https://code.claude.com/docs/en/changelog): ships several times a week (2.1.306 at time of writing).
- [Models overview](https://platform.claude.com/docs/en/models/overview) and [Choosing a model](https://platform.claude.com/docs/en/about-claude/models/choosing-a-model): the current lineup is Fable 5.1 (demanding reasoning, long-horizon agentic work, $10/$50 per MTok), Opus 5.5 (recommended default for most workloads, $4/$20), Sonnet 5.5 (speed and intelligence, $2/$10), Haiku 5.5 (high-volume routing, from $0.10/$0.50). All have 1M-token context.
- [Claude Help Center](https://support.claude.com/) for plan and feature changes; [claude.com/marketplace](https://claude.com/marketplace) for new connectors; [Claude Academy](https://academy.claude.com/) for new courses.
- Practitioners: [One Useful Thing](https://www.oneusefulthing.org/), [Simon Willison](https://simonwillison.net/), and the [Anthropic Discord](https://www.anthropic.com/discord).

### How to evaluate a new model or tool in 30 minutes
1. **Keep a frozen test set** (5 tasks, written once): the Monday brief, a cash forecast from a fixed data file, a customer reply to a tricky email, a lead-triage pass on a fixed list, and a decision memo. Each has a known-good answer you have already approved.
2. **Run the five tasks on the new model** with `/model` in a fresh session (10 min). Do not change prompts.
3. **Score** (10 min): correctness against the known-good answer (pass/fail per task), time to complete, tokens or cost from `/usage`, and number of corrections needed. Anthropic's own prompting docs insist on this order: define success criteria and a way to test them before you tune anything ([prompt engineering overview](https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/overview)).
4. **Decide** (5 min) with the `decide` skill: adopt, watch, or ignore. Log it.

### What to measure, always
- Task pass rate on the frozen set (the quality number).
- Corrections per week (the trust number).
- Approvals that were rubber-stamped versus changed (if you never change anything, promote the task to autonomous; if you change most, demote it).
- Cost per week and per scheduled task from `/usage` attribution.
- Owner minutes per day (the goal is under 20).

### When to switch
- **Model:** switch the default when a new model passes more of the frozen set at equal or lower cost, or passes the same set at materially lower cost. Use the cheaper model for subagents first (the docs recommend Sonnet for teammates and Haiku for exploration), the frontier model for the CEO's planning and decision memos.
- **Tool or connector:** switch when it removes a manual step from the daily 20 minutes or replaces a Chrome-based workflow (less prompt-injection exposure) with a connector.
- **Never switch on launch day for anything customer-facing.** Run the new model on the test set for a week in a parallel scheduled task first.

---

## Part 6. The 10 most common mistakes in AI-operated businesses

1. **Over-automation on day one.** Anthropic's agent guidance: "Begin with the simplest solution, and add complexity only when it's needed," and autonomy "raises costs and the risk of compounding errors" ([Building effective agents](https://www.anthropic.com/research/building-effective-agents)). *Avoid:* every new task starts in approval mode; promote one task per week on evidence.

2. **No verification.** "If you can't verify it, don't ship it." *Avoid:* every task prompt ends with a verification step and an evidence requirement; every scheduled run is opened and read, because a green status only means the session did not crash.

3. **Memory sprawl.** Long, contradictory CLAUDE.md files make Claude ignore the rules that matter; "if two instructions contradict each other, Claude may pick one arbitrarily." *Avoid:* 200-line cap, procedures in skills, path-scoped rules, weekly `/doctor prompt-audit`, auto-memory review in `/memory`.

4. **Cost blowups.** Long sessions resend the full context on every turn; session-scoped loops and cross-session messages fire while idle; agent teams cost about 7x ([costs](https://code.claude.com/docs/en/costs)). *Avoid:* usage credits with a monthly spend limit, `/clear` between tasks, cheaper models for subagents, weekly `/usage` attribution review, and remove connectors a task does not need.

5. **Prompt injection from customer emails, web pages and documents.** Willison's lethal trifecta: private data plus untrusted content plus the ability to send data out equals an exfiltration channel, because models "do not separate instructions from data." A CEO that reads the inbox, has the files, and can send email has all three. *Avoid:* no autonomous sends to external addresses; a hook that blocks outbound email and payments without approval; the Chrome extension only on trusted sites with financial sites blocked; treat fetched content as data (the scheduled-task fire payload is already wrapped as untrusted for this reason).

6. **Over-broad permissions and connectors.** Every connector included in a scheduled task can write "without asking for permission during a run." *Avoid:* scope repos, environment network access and connectors per task; use `permissions.deny` and PreToolUse hooks for hard limits; keep API tokens for task triggers in a secret store.

7. **Compliance and privacy drift.** Customer data in prompts, auto-memory and transcripts; actions taken under your identity ("anything a scheduled task does through your connected GitHub identity or connectors appears as you"). *Avoid:* a CLAUDE.md rule on what customer data may be stored and where; delete memory topic files containing personal data; keep regulated functions (payroll, tax filing, contracts) in approval mode; use the `operations:compliance-tracking` and `small-business:contract-review` skills rather than improvising; remember Claude in Chrome blocks financial-services sites by design.

8. **Skill atrophy in the Owner.** The paradox of supervision: you can only catch what you understand. *Avoid:* Weeks 6 and 7 of the curriculum; do one customer call and one bank reconciliation yourself every month.

9. **Treating the AI as the decision maker.** Anthropic's engineers kept "high-level design, strategic thinking, and decisions that need organizational context." *Avoid:* the CEO proposes with odds via the `decide` skill; the Owner decides; the log records who decided. Mollick: "the people who thrive will be the ones who know what good looks like."

10. **No upgrade loop.** Features ship weekly; the boundary of what can be delegated is "a moving target." *Avoid:* the weekly `upgrade` scan, the frozen test set, and a quarterly re-read of this playbook with the CEO asking "what in here is now wrong?"

---

*Sources are linked inline. Primary Anthropic sources: [anthropic.com/research](https://www.anthropic.com/research), [code.claude.com/docs](https://code.claude.com/docs), [support.claude.com](https://support.claude.com), [academy.claude.com](https://academy.claude.com), [claude.com/pricing](https://claude.com/pricing), [platform.claude.com/docs](https://platform.claude.com/docs).*
