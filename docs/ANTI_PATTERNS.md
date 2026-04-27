# Anti-patterns

## Blind template copying

Copying the templates without inspecting the target repository defeats the kit.

The target repo must be read first.

## State duplication

Do not turn `PROJECT_SKELETON.md` into a second `STATE.md`.

`STATE.md` changes often.
`PROJECT_SKELETON.md` changes only when structure or conceptual architecture changes.

## Roadmap theater

Do not create fake sprint plans just to look organized.

A narrow next step is better than a decorative roadmap.

## Governance inflation

Do not create ten governance files when five are enough.

More files can make reentry harder, not easier.

## Silent scope reopening

If a blocker says "UI is blocked", a local change must not silently reopen UI.

Blocked scope must be reopened only by explicit decision.

## Review without write-back

If a structural change happens and the context files still describe the old structure, the work is incomplete.

## Agent as hidden architect

The agent may recommend.
The agent may execute.
The agent must not secretly redefine the project.
