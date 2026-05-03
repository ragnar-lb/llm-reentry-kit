# RESUME_SESSION

Use this prompt at the start of any new session on a project that already has the reentry kit installed.

This is the most common case: you are returning after a gap, the agent has no memory of previous sessions, and you need it to re-enter safely before doing anything.

---

You are resuming work on a project.

You have no reliable memory of previous sessions.
Do not assume you know the current state.
Do not assume the README is current.
Do not invent context that is not in the files.

## Step 1 — read the standard minimum reentry set

Read each of these files in order before doing anything else:

1. `AGENTS.md`
2. `README.md`
3. `STATE.md`
4. `docs/ops/PROJECT_SKELETON.md`
5. `docs/ops/CONTEXT_SYNC_CHECKLIST.md`

If `CLAUDE.md` exists, read it first — it is the Claude Code entry point and may contain branch-specific instructions.

## Step 2 — report the current state

After reading, report the following clearly and concisely:

- what the project is (one sentence);
- what the current phase is;
- what is actively blocked;
- what is currently allowed;
- the next recommended narrow step from `STATE.md`;
- any contradictions or stale content you noticed in the context files.

Write for a user who may not be a programmer.
Do not use jargon unless it appears in the context files.
Do not recommend structural changes yet.

## Step 3 — ask for today's task

After the state report, ask:

> "What would you like to work on today?"

Wait for the answer.

Then read the task-local files relevant to the request before doing any structural work.

## Constraints

- do not change any files until the state report is complete;
- do not reopen any scope that `STATE.md` marks as blocked;
- do not add runtime code, a CLI, or dependencies unless explicitly authorized by the project owner;
- if you notice a contradiction in the governance files, name it rather than silently resolving it.
