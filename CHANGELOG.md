# Changelog

Changes to criteria, gates, thresholds, bands, or decision rules are listed here with the instrument's new version number. Wording-only fixes are not.

## Toolkit 1.1 · October 2026

### Added

- **AI Authority Review 1.0** ([ai-authority-review/](ai-authority-review/)). The decision meeting the other instruments feed: twelve questions, the eight-dimension Evidence Chain, a six-outcome authority decision, a 45 to 60 minute facilitator guide that opens with the ten-times question, and a completed example. Includes a one-page printable form. This is Appendix A of the book, now published in full.
- **Agent Register 1.0** ([agent-register/](agent-register/)). A Scope Card for every agent before go-live (a scope with an explicit "may never touch" list, an owner, and a tested stop button), an enterprise register with a CSV template, and a quarterly reconciliation that finds agents running without an entry. Core rule: no entry, no credentials.
- **Scorecard workbook** ([scorecard/scorecard-workbook.xlsx](scorecard/scorecard-workbook.xlsx)). A spreadsheet edition of the Readiness Scorecard. Plain formulas, no macros. It totals the score, applies the six gates, names the band and the maximum authority state, and flags a gap between the authority the system holds and the authority its band allows.
- **Worked example** ([examples/](examples/)). One fictional invoice-matching agent followed through all eight instruments, from the Stop Line at funding through a promotion, a suspension, a restore, and a second market. Includes the fully scored example workbook.
- **Start here** table in the top-level README, mapping each common decision to the instrument that answers it.
- This changelog.

### Changed

- **Book title.** Updated to *Enterprise AI Decision System: Turning Capability into Authorized Enterprise Action* across the toolkit and citation metadata.
- **License scope.** The README now states that the MIT License covers the instruments and documentation in this repository, not the text of the book.
- **Agentic AI Production Readiness Scorecard 1.1.** Added the **Expanded-ready** band: a total of 95 or more, every gate at 3, and no criterion at 0, required before any grant of expanded autonomy, with a 60-day sunset on every grant. It is the top of the Production-ready range with a stricter gate condition, not a new score range. Previously this rule appeared only as a sentence under Production-ready. No criterion, anchor, or existing band threshold changed.
- **Contributing guide.** Spreadsheet editions of an instrument are now accepted when they use plain formulas only, contain no macros or external links, and match the written instrument exactly.

## Toolkit 1.0 · October 2026

First public release of six instruments: the Agentic AI Production Readiness Scorecard, Authority Change Record, Vendor Authority Gates, Market Authority Passport, True Cost of an Action, and Stop Memo. Archived on Zenodo, concept DOI [10.5281/zenodo.23464328](https://doi.org/10.5281/zenodo.23464328).
