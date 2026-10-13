# lore round 26 — calibration

Work commit `afe5ed54dddec767fbb4615723e75bcd0e554518` by lore-shokunin <lore@shokunin.local>. Baseline report commit `f44e7281a5438dc86e4fd8a03b19476e4cce7371`. This report is written after the work commit. No push/merge.

## Work performed

- Pre-dispatch claim, wave plans, one-field fixture policy and failure telemetry: `.shokunin/lore/LOG.md` round 26 at `afe5ed54dddec767fbb4615723e75bcd0e554518`. Eight scoped scout reports `.shokunin/lore/reports/r26-{screen-scout,mutation-scout,citation-scout,regression-scout,critic,simplifier,scribe,schema-scout}.md` precede implementation.
- New `corpus/fixtures/r26-to-malformed/` copies `r25-to-ambiguous/` except the second raw `seal` row's `name` becomes `""`; checker remains byte-identical (`reports/r26-executor.md`, `afe5ed54dddec767fbb4615723e75bcd0e554518`). README documents the admitted-row boundary without a canon uniqueness claim.
- Named non-author `reports/r26-reviewer.md` confirmed the single field mutation and limits. `reports/r26-independent-verifier.md` independently replayed old outputs and JSON. First Sol adjudicator child `sub-836a6028` exited without reply/report; logged as failure, not verdict. Replacement non-author Sol `reports/r26-axis-adjudicator-retry.md` reran target triple and admitted narrowly. All reports at `afe5ed54dddec767fbb4615723e75bcd0e554518`.

## Landed changes

- `LOG.md`, `SCORECARD.md`, fixture README, five new fixture JSON files and eleven scoped evidence reports landed in `afe5ed54dddec767fbb4615723e75bcd0e554518`. No checker algorithm edit. This report cites that completed work commit, not itself.

## Before → after measurements

- Before at `f44e728`: no `r26-to-malformed` fixture path (`git ls-tree -r --name-only f44e728 -- .shokunin/lore/corpus/fixtures/r26-to-malformed` → empty); admitted `r25-to-ambiguous` exits 1 with duplicate-ID and `relations[0].to` ambiguity; `r25-to-unique` exits 0. After at `afe5ed54dddec767fbb4615723e75bcd0e554518`: `python3 .shokunin/lore/corpus/fixtures/check_bible.py .shokunin/lore/corpus/fixtures/r26-to-malformed` exits 1 with **only** `entities[4].name: required nonempty str` and `1 violation(s); no canon changed`; no duplicate admitted ID or target ambiguity. The raw second row still exists. Verifier replay: **75/75** prior stdout/stderr/exit exact and **374/374** prior JSON paths byte-identical; five new paths.
- Axis verdict from `r26-axis-adjudicator-retry.md`: **calibration improved**, **depth unchanged**, **coverage unchanged**, none harmed. This admits one screened-row interpretation only, not source-text truth, target uniqueness, or canon.

## SHONEN

- [~] Decision table/error patterns: `corpus/fixtures/README.md` round 26 and `reports/r26-scribe.md`; no promotion review.
- [~] End-to-end task logged and non-author replayed: `LOG.md` round 26, `reports/r26-independent-verifier.md`; no SHONEN checkmark review.
- [~] Executable instructions: fixture README command triple; no promotion review.
- [~] Province boundary: `PROVINCE.md` and `reports/r26-citation-scout.md` keep source-ID versus truth/rights distinct; no promotion review.
