---
name: upgrade
description: Weekly self-upgrade scan. Finds new AI models, Claude Code and Cowork features, MCP connectors, skills and competitor tools, rates each adopt/watch/ignore, and updates the multi-model stack playbook. Use weekly or when a big release drops.
---

# /upgrade — Stay Current

1. Dispatch the Scout with this brief: "Scan the last 7-14 days for: Anthropic releases and the
   Claude Code changelog; new Claude connectors and skills; OpenAI, Google, Meta, xAI and major
   open-weight model releases; notable agent tooling (OpenClaw, n8n, Agent SDK changes); anything
   competitors in our niche are shipping. For each item: what it is, link, and a rating of
   adopt now / watch / ignore with one line of reasoning tied to our thesis."
2. Sources to check first: anthropic.com/news, docs.claude.com changelog (Claude Code), the
   Claude connectors directory, openai.com/news, blog.google (Gemini), ai.meta.com, Hacker News,
   and the X/Reddit threads for Claude Code.
3. Write the report to `company/research/upgrades/{YYYY-MM-DD}.md`.
4. For every "adopt now": add a line to `company/playbooks/multi-model-stack.md` or the relevant
   playbook, and an Owner to-do in `state.md` if it needs a subscription or install.
5. Return the top 3 adoptions to the Owner in three sentences. No listicle.

Judgment rule: adopt only what moves a scorecard number or removes a bottleneck. Shiny is not a
reason.
