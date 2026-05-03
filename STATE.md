# STATE.md

This file records the current operational state of `llm-reentry-kit`.

It is not a changelog.
It is not a roadmap fantasy.
It is not a complete documentation index.

It exists so a future agent can re-enter this repository without guessing.

## Current phase

`v0.4 non-programmer usability pass`

The repository is a public, Markdown-first governance bootstrap kit for LLM-assisted repositories.

## Last stable checkpoint

`v0.1` established the initial public document set:

- README
- AGENTS
- prompts
- templates
- concept docs
- anti-pattern docs

`v0.2` made the repository dogfood its own reentry contract.

`Issue #1` records the final clean dogfood audit after the v0.2 repair cycle and follow-up path-canonicalization pass. It is closed as completed.

`Issue #2` records the adversarial audit that identified terminal-agent governance self-protection gaps. It is closed as completed after adding protected governance path rules and explicit governance-maintenance mode.

## Active blockers

- no CLI yet
- no runtime automation yet
- no package manager integration yet
- no vendor-specific adapter yet
- no broad agent orchestration framework yet

## Current allowed work

- improve prompts
- improve templates
- improve explanatory docs
- add small examples
- tighten the reentry contract
- fix contradictions between governance files
- test the kit on real target repositories and record friction
- run explicit governance-maintenance tasks when governance itself is the target

## Current forbidden work

- do not add runtime code
- do not create a CLI
- do not add dependencies
- do not create a framework
- do not create vendor lock-in
- do not expand into broad AI safety theory
- do not create alternate command documents that compete with `AGENTS.md`
- do not modify protected command files during normal operational work

## Current protected command files

These files may be read during normal operation but may only be changed in explicit governance-maintenance mode:

- `AGENTS.md`
- `README.md`
- `docs/ops/PROJECT_SKELETON.md`
- `docs/ops/CONTEXT_SYNC_CHECKLIST.md`

`STATE.md` is the live state file and remains writable for truthful context write-back.

## Current risks

- the minimal example may become decorative if the kit is not tested on real target repositories
- the kit may become decorative if it stops dogfooding its own rules
- the kit may become overbuilt if automation is added before repeated manual use proves pain
- protected-path discipline is still documentary/operational, not OS-level or Git-hook enforcement

## Next recommended narrow step

Use the kit on one real target repository and record the friction.

Do not automate until the manual prompt/template workflow has been used enough to expose repeated failure points.

## Last stable checkpoint (v0.3)

`Issue #2` closed after adversarial audit. Protected governance path rules and explicit governance-maintenance mode added. Checked set now separates protected command files from the live STATE file.

## What changed in v0.4 (branch `claude/improve-repo-structure-W3Ceb`)

This branch is stewarded by Claude (Anthropic) via Claude Code. Do not modify its files without explicit authorization from the repository owner.

Changes completed:

- `CLAUDE.md` added — Claude Code entry point; declares branch stewardship; does not compete with `AGENTS.md`.
- `examples/minimal-target-repo/` completed — all five standard minimum reentry files present, filled in for a concrete fictional project (invoice-parser); no longer just a text description of what should exist.
- `templates/README.md.template` added — the template set was missing a README template; README is part of the standard minimum reentry set.
- `prompts/RESUME_SESSION.md` added — prompt for resuming work after a session gap; the most common non-programmer use case and previously missing from the kit.
- `templates/CLAUDE.md.template` added — template for a Claude Code entry point in target repositories.
- `docs/HUMAN_GUIDE.md` added — plain-language guide for non-programmer project owners: what a well-behaved agent looks like, red flags, what to say when something is wrong.
- `README.md` patched (governance-maintenance) — added RESUME_SESSION to quickstart; added "For Claude Code users" section.
- `docs/ops/PROJECT_SKELETON.md` patched (governance-maintenance) — added new files to the Core directories listing.

## Next recommended narrow step

Use the kit on one real target repository (stress-test case: 100% LLM-governed) and record the friction.

Do not automate until the manual prompt/template workflow has been used enough to expose repeated failure points.

## Last context write-back

`v0.4 non-programmer usability pass: RESUME_SESSION prompt, CLAUDE.md template, HUMAN_GUIDE, completed example, README template, and governance-maintenance patches to README and PROJECT_SKELETON. Branch claude/improve-repo-structure-W3Ceb.`
