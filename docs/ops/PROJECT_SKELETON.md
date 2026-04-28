# PROJECT_SKELETON

This file is the stable short-map of `llm-reentry-kit`.

It should not duplicate `STATE.md`.
It should change only when the repository structure or conceptual architecture changes.

## What this repository is

`llm-reentry-kit` is a document-only governance bootstrap kit for LLM-assisted repositories.

It helps a coding agent install a minimum reentry/context contract into another repository.

## What this repository is not

This repository is not:

- an application
- a CLI
- an agent runtime
- an orchestration framework
- a vendor-specific integration
- an automatic safety layer

## Core directories

- `prompts/` — copy-paste prompts to run inside target repositories
- `templates/` — adaptable templates for target repository governance files
- `docs/` — concept notes, design notes, anti-patterns, and operational docs for this kit
- `docs/ops/` — live governance files for this repository itself

## Core concepts

- `standard minimum reentry set` — the five files an agent must read before repo-level recommendations or structural work
- `context rehydration` — rebuilding project state from repository files before acting
- `task-local context` — files specific to the slice being changed
- `context write-back` — updating relevant context files after structural or semantic changes
- `dogfooding` — this repository must follow the same governance contract it installs elsewhere

## Non-goals

- implementing automation before the document-only workflow proves useful
- claiming agent safety is solved
- replacing engineering review
- creating process theater
- forcing one project structure onto every repository

## Current structural risks

- examples are still thin
- users may copy templates without target-repo inspection
- agents may ignore the contract because enforcement is documentary, not automatic

## Reentry rule

Before structural or semantic work, read the standard minimum reentry set:

1. `AGENTS.md`
2. `README.md`
3. `STATE.md`
4. `docs/ops/PROJECT_SKELETON.md`
5. `docs/ops/CONTEXT_SYNC_CHECKLIST.md`

Then read task-local context files.

If the agent cannot summarize the current structure honestly, it must not change macrostructure.

After structural or semantic work, update context in the same cycle.
