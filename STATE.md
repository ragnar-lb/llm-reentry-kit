# STATE.md

This file records the current operational state of `llm-reentry-kit`.

It is not a changelog.
It is not a roadmap fantasy.
It is not a complete documentation index.

It exists so a future agent can re-enter this repository without guessing.

## Current phase

`v0.2 document-only bootstrap kit`

The repository is a public, Markdown-first governance bootstrap kit for LLM-assisted repositories.

## Last stable checkpoint

`v0.1` established the initial public document set:

- README
- AGENTS
- prompts
- templates
- concept docs
- anti-pattern docs

`v0.2` makes the repository dogfood its own reentry contract.

`Issue #1` records the final clean dogfood audit after the v0.2 repair cycle and follow-up path-canonicalization pass. It is closed as completed.

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

## Current forbidden work

- do not add runtime code
- do not create a CLI
- do not add dependencies
- do not create a framework
- do not create vendor lock-in
- do not expand into broad AI safety theory

## Current risks

- the minimal example may become decorative if the kit is not tested on real target repositories
- the kit may become decorative if it stops dogfooding its own rules
- the kit may become overbuilt if automation is added before repeated manual use proves pain

## Next recommended narrow step

Use the kit on one real target repository and record the friction.

Do not automate until the manual prompt/template workflow has been used enough to expose repeated failure points.

## Last context write-back

`v0.2 final clean audit checkpoint: live STATE, AGENTS dogfood rule, PROJECT_SKELETON, CONTEXT_SYNC_CHECKLIST, README quickstart, BOOTSTRAP_FROM_SCRATCH prompt, minimal example, canonical ops paths in docs/prompts, and closed Issue #1 audit record are aligned.`
