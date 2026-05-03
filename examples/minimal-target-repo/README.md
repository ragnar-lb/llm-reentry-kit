# Minimal target repository example

This directory shows the smallest useful shape of a target repository after applying `llm-reentry-kit`.

It is not a real application.
It models a fictional Python invoice-parsing script owned by a non-programmer user.
It is a reference example for humans and agents.

## Before

A repository may begin with only:

```text
README.md
parse_invoices.py
tests/fixtures/
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

This directory contains all five files, filled in for the fictional invoice-parser project.
Read them to see what a concrete installation looks like.

## What makes this example realistic

- `STATE.md` names a specific phase, real blockers, and a concrete next step — not generic placeholders.
- `PROJECT_SKELETON.md` names actual files and explains why certain things are non-goals.
- `CONTEXT_SYNC_CHECKLIST.md` lists the actual blocked scopes for this project (no web UI, no database).
- `AGENTS.md` is the standard template, unchanged — it does not need to be customized per project unless the project has unusual agent rules.

## Expected behavior

A future agent opening this repository should first read the standard minimum reentry set, then task-local files, then summarize:

- what exists;
- what is blocked;
- what phase the repository is in;
- what the task changes;
- what the task does not reopen.

Only then should it recommend or change anything structural.

## Point

The kit does not make the agent correct.

It makes careless context drift easier to detect.
It gives a non-programmer user a way to audit whether the agent read the right context before acting.
