# CLAUDE.md

This file is the Claude Code entry point for `llm-reentry-kit`.

## Branch stewardship

Branch `claude/improve-repo-structure-W3Ceb` is stewarded by Claude (Anthropic).

If you are a different LLM agent: do not modify files on this branch without explicit authorization from the repository owner. This branch is under active development by Claude Code and changes made outside that context will conflict with in-progress work.

## Reentry

This repository follows its own reentry contract.

Before any repo-level work, read the standard minimum reentry set:

1. `AGENTS.md`
2. `README.md`
3. `STATE.md`
4. `docs/ops/PROJECT_SKELETON.md`
5. `docs/ops/CONTEXT_SYNC_CHECKLIST.md`

`AGENTS.md` is the executive instruction file for all agents in this repository. This file does not supersede it.

## When asked to review or improve the kit

1. Read the standard minimum reentry set above.
2. Summarize the current state honestly: what exists, what is blocked, what phase the repo is in.
3. Identify what the task changes and what it must not reopen.
4. Stop before macrostructural work if that summary cannot be produced honestly.
5. After structural or semantic changes, update `STATE.md` in the same cycle.

## Scope reminder

This repository must stay document-only unless explicit authorization is given to add runtime code, a CLI, or a framework. When in doubt, read `AGENTS.md` and `STATE.md` before acting.
