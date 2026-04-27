# Concepts

## Context rehydration

The agent rebuilds the current project state from repository files before making recommendations or structural changes.

## Standard minimum reentry set

The smallest stable group of files an agent must read before operating at repo level:

1. `AGENTS.md`
2. `README.md`
3. `STATE.md`
4. `docs/ops/PROJECT_SKELETON.md`
5. `docs/ops/CONTEXT_SYNC_CHECKLIST.md`

## Project skeleton

A stable map of what the repository is, what it is not, and what its main parts do.

## State

The current phase, blockers, allowed work, forbidden work, risks, and next narrow step.

## Context write-back

Updating the relevant context files after a structural or semantic change.

Without write-back, the next agent starts from stale context.

## Task-local context

Files that define the specific slice being changed.

Examples:

- a package README;
- an ADR;
- a module-specific AGENTS file;
- a schema doc;
- a release gate;
- a test fixture README.

Task-local context comes after the standard minimum reentry set, not before it.

## Governance burden

The user should not have to remember the names of context files.

A vague request like "review this repo and tell me what to do next" should be enough to trigger reentry discipline.
