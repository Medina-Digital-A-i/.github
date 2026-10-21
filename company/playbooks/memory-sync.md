# Playbook: Memory Sync (cloud <-> Mac mini)

The repo is the memory. Two facts shape how we keep it in sync:

1. Cloud sessions (claude.ai/code) push to `claude/...` branches, not `main`.
2. The Mac mini reads `main`.

So memory written in the cloud reaches the Mac only after a merge. Procedure:

## Every working session (cloud or Mac)
1. Start: `git pull origin main` (the Mac does this in its launchd script; cloud sessions start
   from a fresh clone of main).
2. Work. Write memory to `company/memory/`.
3. End: commit with a clear message. Cloud: push to the session branch and open a PR titled
   `memory: {date} {one-line summary}`. Mac: push straight to main.

## Merging cloud memory
- The Owner (or the CEO in a later session with the GitHub tools) merges `memory:` PRs promptly.
  Nothing in them is risky: they are text. Review the diff, merge, done.
- If two sessions touched `state.md`, keep both facts and the later date. `decisions.md` and
  `lessons.md` are append-only, so conflicts there are easy: keep both entries.

## Conflict avoidance
- One writer per file per day where possible. Dated files for weekly reviews, decision memos and
  upgrade reports (`company/memory/weekly/`, `company/memory/decisions/`,
  `company/research/upgrades/`) so parallel sessions never collide.
- `state.md` is the only hot file. The Chief of Staff owns it. Others propose edits.

## Per-agent memory
Each agent has `memory: project`, which stores its own notes in `.claude/agent-memory/<name>/`.
That directory is committed, so the Scout's running list of sources, or the Closer's objection
library, travels with the repo.

## What does NOT sync (by design)
- `CLAUDE.local.md` on the Mac: local-only notes, never in git.
- Claude's auto-memory directory: machine-local. Treat it as a cache, not a record.
- Secrets: never in the repo. Environment variables on the Mac; connector settings in claude.ai.
