# Design Notes

## Why this kit exists

LLM coding agents are useful, but they can drift.

They forget context.
They over-trust local files.
They reopen blocked scope.
They mistake stale README text for current project truth.
They make plausible changes that leave the repository harder to re-enter later.

This kit tries to reduce that failure mode by making context reentry explicit and repetitive.

## Why document-first

A document-only kit is boring on purpose.

It can be read by any agent.
It can be adapted to any repository.
It does not need installation.
It does not add runtime dependency.
It does not create another system to maintain.

Automation can come later if the manual protocol proves useful.

## Why five files

The five-file set splits responsibilities:

- `AGENTS.md` tells agents how to behave.
- `README.md` tells humans and agents what the repo is.
- `STATE.md` records the current operational phase.
- `PROJECT_SKELETON.md` records stable structure.
- `CONTEXT_SYNC_CHECKLIST.md` forces before/after discipline.

The goal is not more documentation.
The goal is less hidden context.

## Why this helps non-programmers

A non-programmer using a coding agent often cannot reliably judge whether the agent is making architectural drift worse.

The repository must therefore carry more of the navigation burden.

The agent should be forced to re-enter from written context, state its assumptions, and update the context after meaningful changes.

## Failure modes this kit does not solve

- an agent ignores instructions;
- the user accepts bad changes without review;
- the repository has no tests or gates;
- the project goal is incoherent;
- the installed context files are not maintained;
- a model confidently lies about what it read.

This kit is a guardrail, not a priest.
