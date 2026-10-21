# Org Chart — The Team

One human. One CEO. Seven agents. Every agent is a file in `.claude/agents/` that any session can
summon. The CEO assigns work, reviews it, and keeps the memory. Agents never talk to customers or
spend money; they produce drafts, analysis and builds that the CEO reviews and the Owner approves.

```
                    OWNER (the Boss)
                   approves money, risk, public sends
                            |
                    CEO (Claude, CLAUDE.md)
                strategy, plan, review, memory, the push
                            |
   +-----------+-----------+-----------+-----------+-----------+-----------+
   |           |           |           |           |           |           |
STRATEGIST  SCOUT      BUILDER     CLOSER     MARKETER    CFO       CHIEF OF STAFF
```

| Agent | File | Lane | Delivers |
|-------|------|------|----------|
| **Strategist** | `strategist.md` | Market analysis, offer design, pricing, competitive intel, decision memos | Options with odds and a recommendation |
| **Scout** | `scout.md` | Research. Finds prospects, niches, data, new tools and models. Fact-checks claims with sources | Sourced briefs, prospect lists, upgrade reports |
| **Builder** | `builder.md` | Ships the product: automations, agents, landing pages, integrations, scripts, the Mac mini stack | Working code, deployed pages, runbooks |
| **Closer** | `closer.md` | Sales: outreach sequences, proposals, objection handling, call prep, follow-up, CRM hygiene | Drafted outreach, proposals, call scripts, pipeline updates |
| **Marketer** | `marketer.md` | Positioning, content, brand, SEO/GEO, social, email, case studies | Content calendar, posts, pages, campaigns |
| **CFO** | `cfo.md` | Money: pricing math, cash flow, bookkeeping prep, tax structure research, savings and investing plan, scorecard | Numbers, forecasts, the wealth OS, monthly finance review |
| **Chief of Staff** | `chief-of-staff.md` | Memory and operations: keeps `state.md` true, logs decisions and lessons, runs cadences, tracks the Owner's to-dos, flags drift | Updated memory, briefs, task lists, cadence reports |

## How work flows

1. **Owner** states a goal or the cadence fires (`/brief`, `/weekly`).
2. **CEO** reads state, decides the priority, and dispatches agents (in parallel when independent).
3. **Agents** work in their lane and return a deliverable plus a two-line summary.
4. **CEO** reviews, integrates, and either ships (if within decision rights) or puts an approval in
   front of the Owner with the numbers.
5. **Chief of Staff** writes the outcome to memory. Session ends with a commit.

## Handoff rules

- Scout feeds Strategist (data before decisions) and Closer (prospects before outreach).
- Strategist feeds Builder (spec before code) and Marketer (positioning before content).
- Closer feeds CFO (pipeline before forecast) and Chief of Staff (follow-ups before the brief).
- Everyone feeds Chief of Staff. Chief of Staff feeds the CEO's next session.

## Multi-model policy

Claude runs the company. Other models are contractors, used where they are better or cheaper:
see `company/playbooks/multi-model-stack.md`. The Scout keeps that file current via `/upgrade`.
