# llm-reentry-kit

**A context-governance bootstrap kit for non-programmers building real software with LLM coding agents.**

This repository is a small, document-first kit for people using tools like Codex, Claude Code, Cursor agents, or other LLM coding agents before they fully know how to program.

It does not make agents safe.
It does not replace engineering judgment.
It does not prevent bad decisions automatically.

It gives an agent a minimum operational contract:

- read the repository context before changing structure;
- summarize the current state honestly;
- avoid reopening blocked scope by accident;
- update the repository context after structural or semantic changes.

The goal is simple:

> Make the repository remember what the agent will forget.

## Who this is for

This kit is mainly for people who are building with LLM coding agents while still learning software development.

That does not mean the user is stupid.
It means the user may understand the goal, domain, business problem, or investigation better than the implementation details.

The kit exists to reduce the damage caused when a coding agent acts confident while carrying stale or incomplete context.

## What this kit installs into a target repository

The standard minimum reentry set is:

1. `AGENTS.md`
2. `README.md`
3. `STATE.md`
4. `docs/ops/PROJECT_SKELETON.md`
5. `docs/ops/CONTEXT_SYNC_CHECKLIST.md`

These files form a lightweight context contract for future agent sessions.

## Core rule

Do not trust a long-running LLM to remember the whole project.

Make the target repository store enough stable context for the next agent run to re-enter safely.

## Quickstart

Clone or open this repository next to the target repository, then paste one of the prompts below into your coding agent while the agent is operating inside the target repository.

For a repository with little or no governance:

```text
Read `prompts/BOOTSTRAP_FROM_SCRATCH.md` from `llm-reentry-kit` and apply it to this repository.
Do not add runtime code. Do not create a CLI. Install only the minimal document-level reentry contract.
```

For a repository that already has some documentation or governance:

```text
Read `prompts/AUDIT_EXISTING_GOVERNANCE.md` from `llm-reentry-kit` and audit this repository first.
Do not edit files yet. Report missing files, contradictions, stale state, and the minimum safe patch.
```

For normal installation after audit:

```text
Read `prompts/INSTALL_REENTRY_KIT.md` from `llm-reentry-kit` and apply it to this repository.
Inspect the target repository first. Do not blindly copy templates. Keep the patch minimal and document-only.
```

For tightening an existing installation:

```text
Read `prompts/HARDEN_REENTRY_CONTRACT.md` from `llm-reentry-kit` and patch only governance drift.
Make all reentry files agree on the same standard minimum reentry set.
```

Before merging a governance branch:

```text
Read `prompts/MERGE_READY_REVIEW.md` from `llm-reentry-kit` and review this branch for merge readiness.
Do not edit files unless the review finds a blocking governance issue.
```

## What this kit is not

This is not a framework.
This is not a runtime.
This is not a CLI.
This is not a substitute for architecture review.
This is not magic safety for careless agent work.

It is a document-level operating contract.

## Installation principle

Do not blindly copy templates.

The agent must inspect the target repository first, then adapt the templates to the target repository's actual:

- structure;
- phase;
- blockers;
- risks;
- existing documentation;
- build/test/release posture;
- user constraints.

A generic governance kit that ignores the target repository is just decorative bureaucracy.

## Success condition

After installation, a vague user request such as:

```text
review this repo and tell me what we should do next
```

should trigger the agent to rehydrate context from the standard minimum reentry set before making recommendations or changing structure.

## Repository dogfood

This repository follows its own contract.

Before structural or semantic changes here, agents should read:

1. `AGENTS.md`
2. `README.md`
3. `STATE.md`
4. `docs/ops/PROJECT_SKELETON.md`
5. `docs/ops/CONTEXT_SYNC_CHECKLIST.md`

Then they should read task-local files.

## Residual risk

This kit is documentation and operational discipline.

It is not automatic enforcement.
A bad agent can still ignore it.

The point is to make the correct behavior explicit, visible, repeatable, and auditable.
