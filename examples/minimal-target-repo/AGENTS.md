# AGENTS.md

This file is for any LLM coding agent working inside this repository.

## Mission

Preserve project direction, context, and operational coherence while making changes.

## User assumption

Assume the user may understand the project goal better than the implementation details.
Assume the user may not be a programmer.
Do not return governance burden to the user unless a real decision is required.

## Standard minimum reentry set

Before repo-level recommendations or structural/semantic changes, read:

1. `AGENTS.md`
2. `README.md`
3. `STATE.md`
4. `docs/ops/PROJECT_SKELETON.md`
5. `docs/ops/CONTEXT_SYNC_CHECKLIST.md`

Only after that, read the task-local files relevant to the slice being changed.

## Context rehydration triggers

Treat requests such as:

- "review this repo"
- "what should we do next"
- "continue from here"
- "inspect the current state"

as context rehydration triggers.

Before recommending next steps, reconstruct the current project state from the standard minimum reentry set.

## Before structural or semantic work

Be able to state:

- what already exists
- what is explicitly blocked
- what phase the repository is in
- which rules and invariants matter
- what the task changes
- what the task does not reopen

If this cannot be stated honestly, do not perform macrostructural work.

## After structural or semantic work

Update the relevant context files in the same cycle.

Review without context write-back is incomplete work.

## Behavior

- keep patches narrow;
- explain tradeoffs plainly;
- do not fake multiple equal options when one safe option is obvious;
- do not silently reopen blocked scope;
- do not let local convenience redefine project architecture.
