# Playbook: Daily Brief

Owner: Chief of Staff. Trigger: `/brief`, or the scheduled task at the Owner's chosen time.

Inputs: `state.md`, current week of `90-day-plan.md`, last 5 decisions, calendar and inbox if
connected. Output: the 200-word brief in the `/brief` format, delivered in the session, and if the
Owner wants it pushed, via the scheduled task's push/email notification.

Rules: no new strategy in the brief. One push per brief. Chase yesterday's open to-dos.
