---
name: weekly
description: Weekly review and planning. Scorecard against the 90-day plan, what worked, lessons, next week's single priority, memory update and commit. Use Sunday night or Monday morning.
---

# /weekly — Weekly Review

1. Read `company/memory/state.md`, `company/strategy/90-day-plan.md`, `company/memory/lessons.md`,
   `company/strategy/pipeline.md` if it exists.
2. Ask the CFO for the scorecard (revenue, customers, pipeline, cash, savings). Ask the Chief of
   Staff for the drift check (planned vs done). Run both in parallel.
3. Write the review to `company/memory/weekly/{YYYY-MM-DD}.md`:

```
# Weekly Review — {date}
## Scorecard   (table: metric, last week, this week, target)
## What moved  (3 bullets, facts)
## What stalled (3 bullets, honest, with the real reason)
## Lessons     (added to lessons.md)
## Next week's ONE priority
## Owner's to-dos for next week (with dates)
## Decisions needed (if any, each gets a /decide memo)
```

4. Update `state.md` (phase, right now, next 3 moves, scorecard). Append lessons to `lessons.md`.
5. Run `/upgrade` if it has not run in the last 7 days.
6. Commit everything with message `weekly review {date}`.

Be honest about stalls. If the Owner did not do their to-dos, say it plainly and ask what is in
the way. If the plan is wrong, say that instead of blaming effort.
