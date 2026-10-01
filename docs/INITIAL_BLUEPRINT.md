# Initial research blueprint — proposed v0.1

**Repository:** vanpth008-ehou/NCKH_ChebienTCT  
**Inspection date:** 1 October 2026  
**Owner of scientific decisions:** research lead  
**Status:** planning only; proposed work has not been performed.

## 1. Verified starting point

The GitHub repository metadata reported public visibility, size 0, no language and no license. The contents endpoint explicitly returned “This repository is empty”; the branches endpoint returned an empty list. `main` was configured as the default branch but did not yet exist as a branch.

This contribution introduces README.md, this blueprint, and .gitignore. It supplies no executable code, evidence records, software tests, or completed research conclusions. Proposed folders below should be created only when needed.

## 2. Pilot question and scope lock

Use this question template:

> For [scientific species + authentication basis], using [medicinal part], how does [specified processing method] versus [specified unprocessed comparator] change [selected chemical/quality outcome], and what directly measured biological findings support or limit that interpretation?

Before collecting evidence, fill in:

| Decision | Initial value |
|---|---|
| Vietnamese name and accepted scientific identity | TBD |
| Medicinal part and identification requirements | TBD |
| Processing method, adjuvant, and comparator | TBD |
| Primary chemical or quality outcome | TBD |
| Optional secondary biological outcome | TBD |
| Included study types | Original studies with separately attributable species/preparation data |
| Languages, databases, date limits, search cutoff | TBD; record choices and reasons |
| Scientific reviewer and milestone approver | Research lead; name TBD |

The pilot is a workflow feasibility exercise. It is not a completed systematic review and does not establish clinical efficacy or safety.

### Included initially

- Traceable literature searching and a search log.
- Species/part authentication checks and publication deduplication.
- Full-text availability tracking and explicit screening decisions.
- Extraction of processing conditions and before/after measurements.
- Page/table/figure references, units, comparators, uncertainty, and researcher review.
- A manually prepared evidence table and brief narrative summary.

### Deferred

- Automated multi-database harvesting, PDF downloading, OCR, and AI extraction.
- Multi-herb/formula expansion and unrelated diseases/targets.
- Docking, network pharmacology, molecular dynamics, and mechanistic prediction.
- Experimental SOPs, clinical advice, regulatory claims, and commercialization claims.
- Cloud databases, multiuser accounts, paid APIs, and Windows packaging.

Expansion requires a new scope decision. Predictive work requires a separate novelty audit and rationale first.

## 3. Recommended folders

| Path | What belongs here | Version in Git? |
|---|---|---|
| `docs/INITIAL_BLUEPRINT.md` | This starting plan | Yes |
| `docs/scope.md` | Approved question, eligibility, search boundaries | Yes, after review |
| `docs/decisions.md` | Dated decisions, rationale, approver, deferred requests | Yes, after review |
| `docs/milestones.md` | Acceptance checklists and actual status | Yes |
| `templates/` | Blank search, screening, and extraction forms | Yes |
| `data/examples/` | Explicitly synthetic records for demonstrations | Yes |
| `src/` | Future local application modules | Later |
| `tests/` | Future checks with synthetic fixtures | Later |
| `local_workspace/raw/` | Original PDFs and measurements; preserve unchanged | No |
| `local_workspace/working/` | Screening and extraction working copies | No |
| `local_workspace/exports/` | Reports and frozen evidence snapshots | No |
| `local_workspace/logs/` | Local search/run/error records | No |
| `local_workspace/backups/` | Local checkpoints; also keep a separate-device copy | No |

Prefer a research-data folder outside the checkout, such as `Documents/NCKH_ChebienTCT_Data/`, with the same raw/working/exports/logs subfolders. A backup on the same disk alone is insufficient. This plan's Git exclusions are a secondary safeguard, not a guarantee that files cannot be uploaded.

## 4. Minimum evidence model

Start with separate sheets or CSV files; one row should represent one clearly defined record.

| Register | Minimum fields |
|---|---|
| Search log | Search ID, database, exact query, filters, date, returned count, export filename |
| Publications | Publication ID, title, authors, year, DOI/PMID/URL, language, full-text status, local filename, duplicate group |
| Screening | Publication ID, include/exclude/quarantine, reason, reviewer, date, species/part confidence |
| Processing comparison | Comparison ID, publication ID, scientific name, part, authentication, batch/sample ID, comparator, method, adjuvant and ratio, temperature, time, moisture/drying/storage, source location |
| Outcomes | Outcome ID, comparison ID, assay/analyte, method, before/after values, units, normalization basis, replicates, uncertainty/statistical result, source page/table/figure, reviewer status |

Use stable local IDs, for example PUB-0001, CMP-0001, OUT-0001. These are examples of identifiers, not existing records. One publication may contain multiple comparisons and outcomes.

Record “not reported” separately from “not applicable”; never substitute zero. Preserve the authors' values and units. Keep calculated values in separate fields with their formula. Do not pool values with incompatible units, dry/fresh-weight bases, extraction conditions, or assays. Distinguish analytical, in vitro, animal, and clinical findings. A chemical change alone is not evidence of clinical benefit.

Use **quarantine** when identity, comparator, source reliability, or species-specific attribution cannot be resolved. Reviews may help locate original work but should not replace available original evidence.

## 5. First milestone — M1: manual pilot and frozen scope

**Suggested effort:** 3–5 focused working sessions; actual timing depends on full-text access.  
**Proposed sample:** 5–10 candidate publications; if fewer can be traced, retain all and document the gap. No minimum number of positive studies is required.

1. Approve one species, part, processing comparison, primary outcome, and eligibility rules.
2. Search at least two suitable sources, for example PubMed and Europe PMC; add a relevant Vietnamese source if available. Record exact searches and access limitations. Database availability and relevance must be checked when searching.
3. Register candidates and duplicates; retain accessible full texts locally.
4. Screen each candidate. Extract eligible original evidence only; document exclusions and quarantined records.
5. Manually verify every extracted pilot value against its cited page/table/figure.
6. Freeze a dated pilot snapshot and a one-page findings/gaps summary.
7. Restore the snapshot from a separate backup and confirm that it opens.

**Acceptance checklist — all currently pending:**

- [ ] Scope decisions completed and approved.
- [ ] Search log reproducible and cutoff recorded.
- [ ] Every candidate has a stable ID and screening decision.
- [ ] Every included outcome has a source locator, units, comparator, and review status.
- [ ] Missing information and unresolved identity are explicitly marked.
- [ ] No inference is presented as an experimental result.
- [ ] Frozen evidence table and summary open offline.
- [ ] Separate backup restored successfully.
- [ ] Research lead records PASS, FAIL, or UNCERTAIN.

PASS permits specification of a small local prototype. FAIL returns to the pilot plan. UNCERTAIN leaves the milestone open; do not claim research or implementation is complete. If no eligible evidence exists, a well-documented gap can still demonstrate that the workflow works, but it does not support biological conclusions.

## 6. Local-first workflow for a non-programmer

1. **Keep your own working copy.** Use a normal Windows research folder and a spreadsheet editor. You do not need Python or a terminal for M1.
2. **Separate originals from edits.** Put PDFs and raw measurements in raw; work on copies in working. Name PDFs with publication IDs and retain DOI/URL mappings.
3. **Use internet deliberately.** Search and obtain accessible sources online. Entry, sorting, review, and summaries can remain local. Do not assume downloading a paper grants redistribution rights.
4. **Review before sharing.** This repository is public. Only reviewed documents, blank templates, and synthetic examples belong in it. Keep confidential or unpublished material local.
5. **Make small checkpoints.** At the end of a session, save a dated copy and a short decision note. Back up to another device or an institution-approved destination; test restoration.
6. **Treat GitHub as reviewed history.** After initialization, keep `main` as the accepted baseline. Put later proposals on a separate branch (a separate line of work), review the changed files, then merge only accepted changes. A pull request is the review page for that proposal.
7. **Use AI for bounded tasks.** Supply only needed, permitted excerpts. Ask for one deliverable at a time and stop at the phase boundary. Researchers remain responsible for identity, extraction, and interpretation.

Recommended next specification after M1: a local register that opens an approved CSV, filters by herb/processing method, and exports reviewed rows. Proposed technology: Python desktop interface plus local SQLite, with CSV interchange. These are candidates, not selected dependencies or existing features. The first prototype should need no cloud account or AI API. Search connectors, DOCX generation, and an installer are separate later milestones.

## 7. Controlled software changes after the pilot

Use the user's sequence: **Impact → Scope Lock → Pre-test → Patch → Post-test → Decision**.

- **Impact:** state the requested behavior, affected data, dependencies, risks, and rollback.
- **Scope Lock:** list exact files allowed to change, the maximum change surface, and excluded areas. Stop if the patch needs a wider scope.
- **Pre-test:** use synthetic data to capture current behavior and keep an accepted baseline.
- **Patch:** implement only the locked task; no opportunistic cleanup or chained repairs.
- **Post-test:** repeat the relevant before/after checks, including offline use and protection of originals.
- **Decision:** PASS keeps the change; FAIL reverts the entire patch; UNCERTAIN stays out of main. New errors require rollback and renewed analysis, not another patch layered on top.

For an eventual CSV prototype, meaningful checks include Vietnamese text preservation, no modification of the imported original, explicit missing-value handling, correct filtering/export, and operation with the network disconnected. These checks are proposed; none have been run.

## 8. Immediate next decision

Complete the scope table and approve the M1 plan. Do not start application coding until the manual pilot has established what information must be captured and how success will be checked.
