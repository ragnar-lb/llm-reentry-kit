# MERGE_READY_REVIEW

Use this prompt before merging a governance branch.

---

Review the current branch for merge readiness.

Do not change files unless explicitly instructed.
Do not open new scope.

## Verify

Check:

- only expected governance files changed;
- no product code changed unexpectedly;
- no runtime files changed unexpectedly;
- `AGENTS.md`, `README.md`, `STATE.md`, `docs/ops/PROJECT_SKELETON.md`, and `docs/ops/CONTEXT_SYNC_CHECKLIST.md` agree with each other;
- standard minimum reentry set is named consistently;
- context write-back rule is present;
- no duplicate or stale state language was introduced;
- no existing blocker was silently reopened;
- worktree is clean.

## Final answer

Return:

- `PASS` or `FAIL`;
- files changed;
- merge recommendation;
- exact reason if fail;
- residual risk if pass.
