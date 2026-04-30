# BOOTSTRAP_FROM_SCRATCH

Use this prompt inside a repository with little or no existing governance.

---

You are bootstrapping a minimal LLM reentry and context-governance layer into this repository from scratch.

Do not create runtime code.
Do not create a CLI.
Do not create a framework.
Do not invent process theater.

The user may not be a programmer.
The user may still understand the project goal better than you do.
Your job is to make future agent work safer, clearer, and easier to re-enter.

## Step 1 — inspect the repository

Before editing, inspect the repository and identify:

- what the repository currently appears to be;
- whether it has code, docs, data, or only an empty shell;
- main directories and files;
- likely project purpose;
- current build/test posture, if any;
- missing context needed by future agents;
- obvious risks of agent drift.

If the repository is empty or near-empty, say so plainly and create a minimal governance scaffold.

## Step 2 — install the standard minimum reentry set

Create or update:

1. `AGENTS.md`
2. `README.md`
3. `STATE.md`
4. `docs/ops/PROJECT_SKELETON.md`
5. `docs/ops/CONTEXT_SYNC_CHECKLIST.md`

## Step 3 — keep it honest

Do not pretend the project is more mature than it is.

If the repository is only an idea, write that.
If the repository has no tests, write that.
If the repository has no runtime, write that.
If the next step is unclear, state the smallest reasonable next step.

## Required contract

The installed files must require future agents to:

- read the standard minimum reentry set before repo-level work;
- then read task-local files;
- summarize current state honestly before structural or semantic work;
- stop if the summary cannot be honest;
- update context files after structural or semantic changes.

## Constraints

- patch only governance/docs;
- do not add dependencies;
- do not add code;
- do not add CI;
- do not add package metadata unless explicitly required by the project;
- keep the initial scaffold small.

## Final answer

Return:

- files created;
- files updated;
- current repository phase;
- what remains unknown;
- next recommended narrow step;
- residual risk;
- commit SHA if committed.
