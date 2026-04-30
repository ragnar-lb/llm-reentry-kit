# Minimal target repository example

This directory shows the smallest useful shape of a target repository after applying `llm-reentry-kit`.

It is not a real application.
It is a reference example for humans and agents.

## Before

A repository may begin with only:

```text
README.md
src/
```

The user asks:

```text
review this repo and tell me what we should do next
```

Without a reentry contract, an LLM agent may guess from stale context, over-focus on one file, reopen blocked scope, or invent architecture.

## After

The repository receives the standard minimum reentry set:

```text
AGENTS.md
README.md
STATE.md
docs/ops/PROJECT_SKELETON.md
docs/ops/CONTEXT_SYNC_CHECKLIST.md
```

Future vague requests trigger context rehydration before structural work.

## Expected behavior

A future agent should first read the standard minimum reentry set, then task-local files, then summarize:

- what exists;
- what is blocked;
- what phase the repository is in;
- what the task changes;
- what the task does not reopen.

Only then should it recommend or change anything structural.

## Point

The kit does not make the agent correct.

It makes careless context drift easier to detect.
