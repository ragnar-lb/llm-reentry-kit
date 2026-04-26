# AUDIT_EXISTING_GOVERNANCE

Use this prompt inside a target repository when you want an audit before any edits.

---

Audit this repository for LLM-agent governance readiness.

Do not change files yet.
Do not create files yet.
Do not recommend broad rewrites unless strictly necessary.

The target user may not be a programmer.
Your job is to identify whether the repository can safely guide a future LLM coding agent without relying on hidden memory.

## Audit target model

The standard minimum reentry set should eventually be:

1. `AGENTS.md`
2. `README.md`
3. `STATE.md`
4. `docs/ops/PROJECT_SKELETON.md`
5. `docs/ops/CONTEXT_SYNC_CHECKLIST.md`

## Inspect and report

Report:

- existing governance files;
- missing standard reentry files;
- contradictions between README, state docs, and actual structure;
- stale instructions;
- unclear blockers;
- unclear next step;
- places where an LLM agent could reopen forbidden scope;
- places where context write-back is missing;
- whether docs imply a next step that conflicts with current blockers;
- whether any file duplicates another file's role.

## Maturity classification

Classify the repository as one of:

- `no-governance`
- `partial-governance`
- `conflicting-governance`
- `merge-ready-governance`
- `overbuilt-governance`

## Final answer

Return:

- current governance maturity;
- missing files;
- dangerous contradictions;
- minimum patch recommended;
- files that should not be touched;
- whether installation should proceed now.
