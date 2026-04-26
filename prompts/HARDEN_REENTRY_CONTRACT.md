# HARDEN_REENTRY_CONTRACT

Use this prompt inside a target repository that already has some context-governance docs.

---

Harden the existing reentry contract in this repository.

Do not add new architecture.
Do not add runtime code.
Do not create a framework.
Do not expand the project scope.

## Goal

Make sure all governance files agree on the same standard minimum reentry set:

1. `AGENTS.md`
2. `README.md`
3. `STATE.md`
4. `docs/ops/PROJECT_SKELETON.md`
5. `docs/ops/CONTEXT_SYNC_CHECKLIST.md`

## Patch requirements

Make sure every relevant governance file says:

- read the standard minimum reentry set first;
- then read task-local context;
- summarize state before structural or semantic work;
- do not proceed if the summary cannot be honest;
- write back context after structural or semantic changes;
- review without context write-back is incomplete work.

Patch only contradictions, gaps, or stale wording.

## Constraints

- no product code changes;
- no runtime changes;
- no broad rewrites;
- no new framework docs;
- no duplicate state files;
- no roadmap inflation;
- no fake "process maturity" theater.

## Final answer

Return:

- files changed;
- exact governance gap fixed;
- why the patch is merge-ready;
- residual risk;
- commit SHA if committed.
