# AGENTS.md

This repository is a governance bootstrap kit for LLM-assisted repositories.

Do not treat this repository as an application.
Do not add runtime code unless explicitly requested.
Do not turn this into a framework before the document-only kit proves useful.

## Mission

Help an LLM coding agent install a minimum context-governance layer into another repository.

The target user may not be a programmer.
The target user may be delegating project execution to an LLM coding agent.
The agent must therefore reduce context drift, avoid silent scope expansion, and preserve enough repository state for future work.

## Dogfood rule for this repository

This repository must follow the same reentry discipline it teaches others to install.

Before repo-level recommendations or structural/semantic changes in `llm-reentry-kit`, read:

1. `AGENTS.md`
2. `README.md`
3. `STATE.md`
4. `docs/ops/PROJECT_SKELETON.md`
5. `docs/ops/CONTEXT_SYNC_CHECKLIST.md`

Only after that, read task-local context files.

Before structural or semantic work, be able to summarize:

- what this repository is;
- what this repository is not;
- current phase;
- active blockers;
- what the task changes;
- what the task does not reopen.

If that summary cannot be produced honestly, do not change macrostructure.

After structural or semantic changes, update the relevant context files in the same cycle.

## Protected governance paths

During normal operational work, an agent may read all governance files but must not modify the command/control contract that governs its own behavior.

Protected command files in this repository:

- `AGENTS.md`
- `README.md`
- `docs/ops/PROJECT_SKELETON.md`
- `docs/ops/CONTEXT_SYNC_CHECKLIST.md`

`STATE.md` is different: it is the live state file and may be updated for truthful context write-back after structural or semantic changes.

Do not treat `STATE.md` as permission to rewrite the governing contract.

Changing protected command files requires explicit governance-maintenance mode.
A governance-maintenance task must:

1. name the protected file being changed;
2. state why the existing rule is insufficient;
3. keep the patch narrow;
4. update `STATE.md` in the same cycle;
5. leave an audit trail through an issue or equivalent checkpoint when the change affects repository governance.

Do not create alternate command surfaces that duplicate or supersede `AGENTS.md`.
If agent-facing operational rules need hardening, update `AGENTS.md` and the relevant context files instead.

## Standard target files

The standard minimum reentry set for a target repository is:

1. `AGENTS.md`
2. `README.md`
3. `STATE.md`
4. `docs/ops/PROJECT_SKELETON.md`
5. `docs/ops/CONTEXT_SYNC_CHECKLIST.md`

## Non-negotiable rule

Do not blindly copy templates into a target repository.

First inspect the target repository.
Then adapt the templates to the target repository's actual structure, phase, blockers, risks, and existing documentation.

## Reentry contract

Any future agent operating in the target repository should be instructed to:

1. read the standard minimum reentry set;
2. add task-local context files;
3. summarize the current project state honestly;
4. identify what is blocked;
5. identify what the task changes;
6. identify what the task does not reopen;
7. avoid structural work if it cannot produce that summary honestly;
8. update context files after structural or semantic changes.

Review without context write-back is incomplete work.

## Audience rule

Write for a tired human who may not know programming jargon.

Do not patronize the user.
Do not fake neutrality when one safe technical choice is obvious.
Do not return governance burden to the user unless a real decision is required.

The user's lack of programming fluency is not permission for agent improvisation.

## Scope discipline

This repository should remain small.

Allowed work:

- improving prompts;
- improving templates;
- improving explanatory docs;
- tightening terminology;
- adding examples when they prove useful;
- running explicit governance-maintenance tasks when governance itself is the target.

Blocked by default:

- CLI implementation;
- runtime automation;
- agent orchestration framework;
- vendor-specific lock-in;
- broad "AI safety" theory;
- decorative process documents;
- alternate command documents that compete with `AGENTS.md`.

If automation becomes necessary later, document the pain first.
