# PROJECT_SKELETON

This file is the stable short-map of `invoice-parser`.

It should not duplicate `STATE.md`.
It should change only when this repository's structure or conceptual architecture changes.

## What this repository is

`invoice-parser` is a Python script that reads PDF invoices from a local directory and extracts structured line items into a CSV file.

Its primary user is a small business owner who receives invoices from two vendors and wants to import the data into a spreadsheet without manual entry.

## What this repository is not

- not a web application
- not a database
- not a multi-user system
- not a general-purpose document parser
- not a cloud service

## Core directories and files

- `parse_invoices.py` — main script; entry point.
- `README.md` — setup and usage instructions for a non-programmer user.
- `STATE.md` — current phase, blockers, allowed work, and next narrow step.
- `AGENTS.md` — operating instructions for LLM coding agents.
- `docs/ops/PROJECT_SKELETON.md` — stable structure map (this file).
- `docs/ops/CONTEXT_SYNC_CHECKLIST.md` — before/after governance gate.
- `tests/` — automated tests (in progress).
- `tests/fixtures/` — sample PDF invoices used for testing.

## Core concepts

- invoice — a PDF from vendor A or vendor B.
- line item — one row in the invoice (description, quantity, unit price, total).
- CSV output — the structured file written to `output/` after parsing.
- vendor format — vendor A and vendor B use different PDF layouts.

## Current non-goals

- no web UI
- no database storage
- no multi-vendor expansion beyond A and B until A and B are stable
- no deployment

## Current structural risks

- vendor B format is not yet confirmed with real sample files
- no test coverage means regressions will be silent
- the output CSV schema is not documented and may drift
