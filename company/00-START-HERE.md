# Start Here — How This Company Works

This repo is the brain and the memory of Medina Digital AI. It is read by Claude in every session,
in the cloud (claude.ai/code) and on the Mac mini. If it is written here, the CEO remembers it.

## How to use it

1. **Open a session** (cloud or local), and say what you want. The CEO loads `CLAUDE.md`, reads
   the current state, and picks up where it left off.
2. **Run the cadence.** `/brief` in the morning. `/weekly` on Sunday night or Monday morning.
   `/upgrade` once a week. `/decide` when a real choice is on the table.
3. **Do your part.** The CEO will give you a short list of things only a human can do: open the
   bank account, approve a spend, take a sales call, sign. Do them fast. Speed is the edge.
4. **Trust the memory.** Everything lands in `company/memory/`. Read `state.md` any time you want
   to know where things stand.

## Map

```
CLAUDE.md                     CEO standing brief, loaded every session
company/
  charter.md                  mission, roles, decision rights, cadence
  strategy/thesis.md          what we are building and why
  strategy/90-day-plan.md     the plan, week by week
  team/org-chart.md           the agents and how work flows
  memory/state.md             current state (updated every session)
  memory/decisions.md         decision log
  memory/lessons.md           what we learned
  memory/boss-profile.md      what the CEO knows about you
  playbooks/                  repeatable procedures
  wealth/wealth-os.md         entity, tax, investing checklist
  research/                   the research behind the strategy
.claude/agents/               the team (one file per agent)
.claude/skills/               slash commands
```

## Where to work: cloud vs chat vs Mac mini

- **Build and run the company here** (claude.ai/code cloud sessions or Claude Code on the Mac).
  This is where the memory lives, where agents run, and where scheduled tasks fire.
- **Use regular Claude chat for thinking out loud.** Brainstorm, vent, rehearse a pitch. Then bring
  the conclusion back here and tell the CEO to log it.
- **Mac mini = always-on worker.** Install Claude Code, clone this repo, run the daily brief on a
  schedule. Setup steps are in `company/playbooks/mac-mini-setup.md`.
