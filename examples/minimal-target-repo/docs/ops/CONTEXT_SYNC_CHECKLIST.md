# CONTEXT_SYNC_CHECKLIST

Use this checklist before and after structural or semantic changes in `invoice-parser`.

This checklist is intentionally small.
It is not a process framework.
It is a gate against stale context and silent scope expansion.

## Before structural or semantic work

Confirm:

- I read `AGENTS.md`
- I read `README.md`
- I read `STATE.md`
- I read `docs/ops/PROJECT_SKELETON.md`
- I read `docs/ops/CONTEXT_SYNC_CHECKLIST.md`
- I read the task-local context files for the slice being changed
- I can state what this repository is
- I can state what this repository is not
- I can state the current phase
- I can state the active blockers
- I can state what this task changes
- I can state what this task does not reopen

If not, stop before changing macrostructure.

## After structural or semantic work

Confirm:

- the change stayed within declared scope
- no blocked area was silently reopened (no web UI, no database, no deployment work)
- no new dependency was added without discussion
- the relevant context files were updated
- `STATE.md` still describes the real current state
- `PROJECT_SKELETON.md` still describes stable structure accurately
- `README.md` still matches actual usage

## Closing rule

A structural or semantic change is not complete until context write-back is complete.

Review without context write-back is incomplete work.
