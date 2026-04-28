# STATE.md

This file records the current operational state of `llm-reentry-kit`.

It is not a changelog.
It is not a roadmap fantasy.
It is not a complete documentation index.

It exists so a future agent can re-enter this repository without guessing.

## Current phase

`v0.2-dogfood`

The repository is a public, document-only bootstrap kit for installing LLM context-governance into other repositories.

The current work is to make this repository dogfood its own standard minimum reentry contract and improve first-use clarity.

## Last stable checkpoint

`417187708f7c8c0f09f72eb8da584f4890eb7714`

Initial public document-only kit exists on `main` with:

- README
- AGENTS
- license
- install/audit/harden/merge-review prompts
- target repository templates
- concept/design/anti-pattern docs

## Active blockers

- no CLI yet
- no runtime automation yet
- no package manager setup yet
- no vendor-specific agent integration yet
- no claims of automatic enforcement

## Current allowed work

- improve prompts
- improve templates
- improve examples
- clarify quickstart usage
- tighten reentry language
- add dogfood governance files for this repository

## Current forbidden work

- adding runtime code
- adding a CLI
- adding dependencies
- turning the kit into an orchestration framework
- broad AI safety theory
- productizing before the document-only workflow proves useful

## Current risks

- the kit may look abstract without a concrete example
- target agents may still ignore documentation
- users may blindly copy templates instead of inspecting target repositories
- governance files may drift if structural changes do not update this state

## Next recommended narrow step

Finish the `v0.2-dogfood` patch:

- add live `PROJECT_SKELETON`
- add live `CONTEXT_SYNC_CHECKLIST`
- add a copy-paste quickstart to `README.md`
- add `BOOTSTRAP_FROM_SCRATCH.md`

## Last context write-back

Created during `codex/v0.2-dogfood-quickstart`.
