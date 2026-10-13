# lore round 36 — calibration

Work commit `95e7203270045f26e9beb2fcc37269563ef8acec` by lore-shokunin <lore@shokunin.local>. Baseline report commit `356f75b32afed9abb85687689c8d5f55965c0cb3`. This report was written after the work commit. No push/merge.

## Work performed

- Pre-dispatch claim and eight leaf scopes: `.shokunin/lore/LOG.md` round 36 at `95e7203270045f26e9beb2fcc37269563ef8acec`. Reports `.shokunin/lore/reports/r36-{date-scout,ledger-scout,pair-scout,regression-scout,critic,simplifier,scribe,citation-scout}.md` bounded a wrong-date control and rejected checker/canon overreach.
- Added `corpus/fixtures/r36-bell7-wrong-date/` cloned from r35, with a single inherited-file edit: Sella's newly authored excerpt changes seventh to **eighth** day of Embermonth, year 12. Five JSON tables are byte-identical to r35, including Sella's seventh-day event description and ledger rationale. Added editorial `date-contrast-map.md`; README documents the prose/record mismatch. No checker change (`reports/r36-executor.md`, `95e7203270045f26e9beb2fcc37269563ef8acec`).
- Named non-author `reports/r36-reviewer.md` passes the calibration case while rejecting a shared-ringing inference from r36 source texts. `reports/r36-independent-verifier.md` replayed baseline; `reports/r36-axis-adjudicator.md` independently replayed and judged axes. All at `95e7203270045f26e9beb2fcc37269563ef8acec`.

## Landed changes and measurements

- LOG declaration/policy/closure, SCORECARD calibration row, README, ten new fixture artifacts and eleven scoped reports landed at `95e7203270045f26e9beb2fcc37269563ef8acec`. No old JSON/checker edit; this report cites the completed work commit, not itself.
- Baseline `356f75b`: no r36 fixture (`git ls-tree -r --name-only 356f75b -- .shokunin/lore/corpus/fixtures/r36-bell7-wrong-date` → empty). At `95e7203270045f26e9beb2fcc37269563ef8acec`, `python3 .shokunin/lore/corpus/fixtures/check_bible.py .shokunin/lore/corpus/fixtures/r35-bell7-conflict` and its r36 counterpart both exit 0 with exact CLEAN stdout and empty stderr **structurally only**. Five r35/r36 JSON files byte-identical, sole inherited Sella excerpt date edit. Verifier and adjudicator found **87/87** old stdout/stderr/exit exact and **434/434** old JSON bytes unchanged.
- Per-axis verdict: **calibration improved**, **depth unchanged**, **coverage unchanged**, none harmed. Tarin's seventh-day report and Sella's eighth-day report do not establish a single shared ringing; Sella's retained “that same” phrase is in tension with her explicit date. Copied seventh-day event/ledger statements are unsupported by the altered excerpt, not canonically false. No claim that two actual dates/events occurred, no winner, source truth, envelope content or Blue Seal link.

## SHONEN

- [~] Decision table/error patterns: `date-contrast-map.md`, `reports/r36-scribe.md`; no promotion review.
- [~] End-to-end task non-author reviewed/replayed: LOG round 36, `reports/r36-independent-verifier.md`; no SHONEN checkmark review.
- [~] Executable instructions: fixture README round 36; no promotion review.
- [~] Province boundary: `PROVINCE.md`, `reports/r36-citation-scout.md`; no canon/real-world rights/game mechanics claim; no promotion review.
