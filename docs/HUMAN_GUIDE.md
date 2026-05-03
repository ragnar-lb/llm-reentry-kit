# Human Guide

This guide is for the person who owns the project, not the agent.

You do not need to know how to code to use it.
You need to know what to watch for.

---

## What a well-behaved agent looks like at the start of a session

Before making any structural changes, a well-behaved agent should:

1. Read the five governance files (`AGENTS.md`, `README.md`, `STATE.md`, `PROJECT_SKELETON.md`, `CONTEXT_SYNC_CHECKLIST.md`).
2. Report what the project is, what phase it is in, what is blocked, and what the next step is.
3. Ask what you want to work on, or proceed with the stated next step if it is obvious.

If the agent skips steps 1 and 2 and starts making changes immediately, that is a problem.

---

## Red flags

These are signs the agent may be operating on stale or wrong context.

**It starts recommending changes without first summarizing the current state.**
Ask it to read the governance files and report first.

**It proposes work that `STATE.md` explicitly marks as blocked.**
Point to the blocked section and ask it to explain why it thinks the scope is open.

**It describes the project differently from `README.md` or `STATE.md`.**
Ask which file it read and when. It may have skipped reentry.

**It changes `AGENTS.md`, `README.md`, `PROJECT_SKELETON.md`, or `CONTEXT_SYNC_CHECKLIST.md` without naming it as a governance-maintenance task.**
These files are protected. Ask it to revert and explain what governance-maintenance mode requires.

**After making changes, it does not update `STATE.md`.**
The next session will start from stale context. Ask it to update `STATE.md` before finishing.

**It says "it depends on your preference" about a decision that has an obvious safe answer.**
This is sometimes legitimate. Sometimes it is the agent avoiding a decision it should make. Ask it which answer it would choose and why.

---

## What to say when you notice a red flag

You do not need technical language. These plain requests work:

> "Before we continue — read the reentry files and tell me what state the project is in right now."

> "Which files did you read before making that recommendation?"

> "Does `STATE.md` say that work is allowed right now?"

> "You changed a protected file. What is governance-maintenance mode, and did this qualify?"

> "Before we stop — does `STATE.md` still describe the real state of the project?"

---

## What to do at the start of every new session

Paste this into the agent before describing your task:

```
Read `prompts/RESUME_SESSION.md` from this repository and follow it.
```

Or, if the reentry kit has been installed in your target repository, paste this into the agent while it is inside that repository:

```
Read AGENTS.md, README.md, STATE.md, docs/ops/PROJECT_SKELETON.md, and docs/ops/CONTEXT_SYNC_CHECKLIST.md.
Summarize the current state of the project before doing anything else.
```

---

## What this kit does not protect you from

- an agent that ignores instructions;
- changes you accept without reviewing;
- a project goal that is incoherent from the start;
- a model that confidently lies about what it read.

The kit reduces silent context drift.
It does not replace your judgment.

You are the decision-maker. The agent is the executor.
When you are unsure whether to accept a change, ask the agent to explain what it changed, why, and what it did not touch. That explanation is auditable.
