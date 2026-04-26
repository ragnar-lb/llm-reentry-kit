# INSTALL_REENTRY_KIT

Copy this prompt into the LLM coding agent while it is operating inside the target repository.

---

You are installing a standard LLM reentry and context-governance contract into this repository.

Do not blindly copy templates.
Do not invent a framework.
Do not open unrelated work.
Do not return governance burden to the user.

The user may not be a programmer.
The user may still understand the project goal better than you do.
Your job is to make the repository easier for future agents to re-enter safely.

## Phase 1 — inspect first

Before editing files, inspect the target repository and identify:

- what this repository is;
- what this repository is not;
- current phase;
- active blockers;
- main directories and their roles;
- existing documentation and governance files;
- build/test/release posture, if any;
- likely drift risks for future LLM agents;
- places where an agent might reopen blocked scope by accident.

If the repository already has governance files, do not overwrite them blindly.
Integrate with them.

## Phase 2 — create or update the standard minimum reentry set

Create or update:

1. `AGENTS.md`
2. `README.md`
3. `STATE.md`
4. `docs/ops/PROJECT_SKELETON.md`
5. `docs/ops/CONTEXT_SYNC_CHECKLIST.md`

The installed contract must make future vague requests such as:

- "review this repo";
- "figure out what we should do next";
- "inspect the current state and continue";
- "continue from here";

trigger context rehydration before recommendations or structural work.

## Standard minimum reentry set

Every future repo-level recommendation or structural/semantic change must start by reading:

1. `AGENTS.md`
2. `README.md`
3. `STATE.md`
4. `docs/ops/PROJECT_SKELETON.md`
5. `docs/ops/CONTEXT_SYNC_CHECKLIST.md`

Only after that may the agent read task-local context files.

## Required pre-work summary

Before any structural or semantic change, the agent must be able to summarize:

- what exists;
- what is blocked;
- what phase the repository is in;
- which rules and invariants matter;
- what the task changes;
- what the task does not reopen.

If the agent cannot summarize that honestly, it must not perform macrostructural work.

## Required write-back rule

After any structural or semantic change, the agent must update the relevant context files in the same cycle.

Review without context write-back is incomplete work.

## Constraints

- keep the patch minimal;
- preserve existing project language and conventions;
- do not duplicate existing docs unnecessarily;
- do not create fake process bureaucracy;
- do not add runtime code;
- do not create a CLI;
- do not modify product code unless strictly necessary to correct documentation references;
- prefer clear operational writing over abstract theory.

## Final answer

After execution, answer with:

- files created;
- files updated;
- what the installed reentry contract now requires;
- what was deliberately not changed;
- any residual risk;
- whether the worktree is clean;
- commit SHA if you committed.
