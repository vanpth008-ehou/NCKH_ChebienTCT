# NCKH_ChebienTCT

Traditional-medicine processing research (nghiên cứu chế biến cổ truyền): organize traceable evidence on how processing changes medicinal-material composition, analytical quality, and biological effects.

## Status — planning only

Inspection on 1 October 2026 confirmed an empty repository: no files or branches; GitHub configured `main` as the default branch. This initial contribution contains planning documents and Git exclusion rules only. No application, search engine, experimental dataset, tests, or Windows installer has been implemented.

## Proposed first scope

Choose **one medicinal species, one medicinal part, and one processing comparison** (unprocessed versus a defined processed preparation). Record processing conditions, analytical methods, outcomes, and evidence limitations with source/page references. These choices remain **TBD** until the research lead approves them.

First milestone: freeze the pilot question and manually review 5–10 candidate publications, or all traceable candidates if fewer exist. Completion requires a documented search, screening decisions, an evidence table, and a verified backup—not a working app. See the [blueprint and acceptance checklist](docs/INITIAL_BLUEPRINT.md).

## Proposed organization

| Location | Purpose | Status |
|---|---|---|
| `README.md` | Entry point and project status | Added in this planning contribution |
| `docs/` | Scope, milestones, decisions, workflow | Blueprint added; other documents proposed |
| `templates/` | Blank screening and extraction forms | Proposed |
| `data/examples/` | Clearly labelled synthetic demonstration records | Proposed |
| `src/` | Future local application | Proposed; no code |
| `tests/` | Future checks using synthetic data | Proposed; no tests |
| `local_workspace/` | PDFs, real data, exports, backups on your computer | Proposed; excluded from Git |

## Start without programming

1. Read the blueprint; approve the herb, part, comparison, and question.
2. Keep research files in a local Windows folder outside the Git checkout; use Excel or LibreOffice for the pilot.
3. Search online when needed; retain only lawfully accessible full texts locally.
4. Review evidence and uncertainties manually; back up and freeze the pilot.
5. Specify and review one small software feature only after the pilot passes.

Routine organization and evidence entry are intended to work offline without AI calls. Online literature searches and optional GitHub synchronization need internet access. AI can help draft or build later; a researcher verifies every scientific claim.

This repository is **public**. Commit only reviewed planning material and safe examples. Keep participant information, unpublished laboratory data, credentials, and restricted full texts outside it. `.gitignore` helps prevent accidental tracking; it is not access control. No license has been selected.
