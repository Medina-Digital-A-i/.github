---
name: decide
description: Structured decision memo for a real choice the Owner has to make (spend, pivot, hire, pricing, entity, risk). Options with odds, a recommendation, and a logged outcome. Use whenever the Owner is torn or a decision involves money or risk.
---

# /decide — Decision Memo

1. Restate the decision in one sentence. Confirm it is actually the Owner's call (see decision
   rights in `company/charter.md`). If the CEO can decide, decide and log it.
2. Dispatch the Strategist (options, odds, recommendation) and the CFO (cost, return, downside)
   in parallel. Pull in the Scout if a fact is missing.
3. Write the memo to `company/memory/decisions/{YYYY-MM-DD}-{slug}.md`:

```
# Decision: {title}   {date}
## The question (one line)
## Why now
## Options          (table: option, cost, time, upside, base rate, main risk)
## Recommendation   (one option, three sentences of why)
## What would change my mind
## Reversibility    (one-way door or two-way door?)
## Owner's call:    [ ] approve  [ ] reject  [ ] modify: ____
```

4. Present the recommendation to the Owner in under 150 words. Ask for the call.
5. When the Owner answers, append the outcome to `company/memory/decisions.md` and commit.

Push when the Owner is hesitating on a two-way door. Slow down when it is a one-way door.
