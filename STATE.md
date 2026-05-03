# STATE.md

This file records the current operational state of `llm-reentry-kit`.

It is not a changelog.
It is not a roadmap fantasy.
It is not a complete documentation index.

It exists so a future agent can re-enter this repository without guessing.

## Current phase

`v0.4 first external dogfood target`

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

`Issue #4` records the first external dogfood application: bootstrapping the kit into `ragnar-lb/llm-reentry-kit-test`, an empty/private controlled stress-test repository.

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

- the first external dogfood target was empty, so it does not prove behavior on messy existing repositories
- the kit may become decorative if it is not tested against conflicting instructions, placeholder leakage, and terminal-agent write restrictions
- the kit may become overbuilt if automation is added before repeated manual use proves pain
- protected-path discipline is still documentary/operational, not OS-level or Git-hook enforcement

## Next recommended narrow step

Ask an independent agent to review `ragnar-lb/llm-reentry-kit-test` and propose the next step.

Expected behavior: the agent should identify it as a stress-test target and should not invent product/application scope.

Do not automate until the manual prompt/template workflow has been used enough to expose repeated failure points.

## Last context write-back

`v0.4 external dogfood checkpoint: the kit was installed into llm-reentry-kit-test, the target was rechecked, friction was recorded in Issue #4, and the next narrow test is independent-agent review of the target repository.`
