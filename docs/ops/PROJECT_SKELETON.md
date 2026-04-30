# PROJECT_SKELETON

This file is the stable short-map of `llm-reentry-kit`.

It should not duplicate `STATE.md`.
It should change only when this repository's structure or conceptual architecture changes.

## What this repository is

`llm-reentry-kit` is a public, Markdown-first bootstrap kit for installing lightweight context-governance into repositories operated with LLM coding agents.

Its primary audience is people building real software with coding agents before they fully know how to program.

## What this repository is not

- not an application
- not a runtime
- not a CLI
- not a package manager integration
- not a vendor-specific agent adapter
- not a broad AI safety framework
- not a replacement for engineering judgment

## Core directories and files

- `README.md` — human-facing project overview and quickstart.
- `AGENTS.md` — operating instructions for agents working on this kit.
- `STATE.md` — current operational phase, blockers, allowed work, risks, and next narrow step.
- `prompts/` — copy-pasteable prompts for applying the kit to target repositories.
- `templates/` — adaptable target-repository file templates.
- `docs/` — explanatory notes, concepts, and anti-patterns.
- `docs/ops/` — this repository's own live reentry and context-sync documents.
- `examples/` — small examples showing how the kit may look when applied.

## Core concepts

- context rehydration — rebuilding repository state from files before recommendations or structural changes.
- standard minimum reentry set — the five-file set future agents must read before repo-level work.
- task-local context — files specific to the slice being changed, read after the standard set.
- context write-back — updating relevant context files after structural or semantic changes.
- dogfooding — this repository must follow the same reentry contract it teaches others to install.

## Standard minimum reentry set

Before repo-level recommendations or structural/semantic work in this repository, read:

1. `AGENTS.md`
2. `README.md`
3. `STATE.md`
4. `docs/ops/PROJECT_SKELETON.md`
5. `docs/ops/CONTEXT_SYNC_CHECKLIST.md`

Only after that, read task-local context files.

## Current non-goals

- no CLI implementation
- no runtime automation
- no package publishing
- no agent orchestration framework
- no vendor lock-in
- no broad theory expansion

## Current structural risks

- the kit can become too abstract if examples are not kept practical
- the kit can become decorative if it stops dogfooding its own rules
- the kit can become overbuilt if automation arrives before repeated manual use proves pain

## Reentry rule

Before structural or semantic work:

1. rehydrate context from the standard minimum reentry set;
2. add task-local context files;
3. summarize what exists, what is blocked, what phase the repo is in, what the task changes, and what it does not reopen;
4. stop before changing macrostructure if that summary cannot be honest.

After structural or semantic work:

1. update the relevant context files in the same cycle;
2. leave the repository in a state that the next agent can re-enter without guessing.
