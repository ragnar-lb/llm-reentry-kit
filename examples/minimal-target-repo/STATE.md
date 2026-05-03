# STATE.md

This file records the current operational state of `invoice-parser`.

It is not a changelog.
It is not a roadmap fantasy.
It is not a complete documentation index.

It exists so a future agent can re-enter the project without guessing.

## Current phase

`early prototype — core parsing works, no tests, no deployment`

The repository contains a Python script that reads PDF invoices and extracts structured line items into a CSV. It runs locally. Nothing is deployed. No tests exist yet.

## Last stable checkpoint

`initial script passing manual checks on three sample invoices from vendor A`

## Active blockers

- no automated tests yet
- no handling of vendor B invoice format yet
- no error handling for malformed PDFs
- deployment not started

## Current allowed work

- add tests for existing parsing logic
- add handling for vendor B format
- improve error messages when parsing fails
- update this STATE.md after any structural change

## Current forbidden work

- do not add a web UI
- do not add a database
- do not deploy until tests pass
- do not add dependencies without discussing with the project owner
- do not reopen deployment scope before tests are stable

## Current risks

- the manual test samples may not cover edge cases
- vendor B format is guessed, not confirmed — may need sample files before coding
- no error handling means silent failures are possible

## Next recommended narrow step

Write at least three automated tests for the existing parsing logic against the sample invoices already in `tests/fixtures/`.

## Last context write-back

`reentry kit installed; STATE reflects manual-test-only phase as of initial bootstrap`
