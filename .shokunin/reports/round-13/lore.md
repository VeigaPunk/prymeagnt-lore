# lore — round 13 (calibration axis-move)

Declared before dispatch in `.shokunin/lore/LOG.md`. Baseline report commit `97f766762ac78ab6bcf6523aadbd2ffa92d4f4f5` reported dangling actor references yet still asserted `double-booked` for two same-tick different-place events using that absent actor ID.

## Work performed
- At work commit `6b2331a98891f5120015b6de32afd977cecb2ae6`, changed the occupancy guard to run only when exactly one required-field-screened entity row matches `timeline.entity_id`. Zero retains dangling findings and raw events but skips definite occupancy; >1 retains round-12 ambiguity; one retains double-booking. No new warning, lore fact, or canon selection.
- Added fictional pair `corpus/fixtures/r13-{missing-actor,unique-actor}/`, bounded docs/table, saved 28-case CLI outputs `corpus/live/runs/20261012T180109Z/`, and scoped scout/executor/non-author reviewer/verifier/axis reports `reports/r13-*.md`, same work commit. All lanes settled without reported failure.

## Landed changes
- `.shokunin/lore/LOG.md`, `.shokunin/lore/SCORECARD.md`, checker, fixture pair, docs, run outputs and reports at work commit `6b2331a98891f5120015b6de32afd977cecb2ae6`. This report lands last and cites that hash. No push or merge.

## Before → after / independent checks
Run `python3 .shokunin/lore/corpus/fixtures/check_bible.py .shokunin/lore/corpus/fixtures/<case>`. At baseline `97f7667`, `r13-missing-actor` exited 1 with two dangling `unlisted` findings plus definite `double-booked`; current output exits 1 with the two dangling findings only. `r13-unique-actor` remains exit 1 with `double-booked 'mira'`. Non-author verifier compared all 26 prior fixtures byte-identically on stdout/stderr/exit against extracted baseline checker, confirmed pair differs only by actor tokens, and captured unchanged before/after hashes for 139 fixture JSON files. Reviewer probed mixed schedules, unrecognized-kind screened rows, malformed excluded rows and the possible hidden real conflict. See `reports/r13-independent-verifier.md`, `reports/r13-reviewer.md`.

- **Calibration improved:** missing actor no longer causes a definite same-actor inference. A true conflict remains possible and unassessed, not refuted.
- **Coverage unchanged:** uniquely identified actors retain occupancy rule; dangling finding remains.
- **Depth unchanged:** no new substantiated narrative. None harmed; admit with those limits. Required-field-screened row count is not verified character/canon identity or source-text truth.

## SHONEN
- [~] Real decision tables/error patterns/checklists with cited sources — `corpus/knowledge/2026-10-12-lore-decision-table.md`, `reports/r13-reviewer.md`; no box checked.
- [~] End-to-end domain task executed and logged — `corpus/live/runs/20261012T180109Z/`, `reports/r13-independent-verifier.md`; no box checked.
- [~] Instructions executable without oral context — `corpus/fixtures/README.md`; no box checked.
- [~] No cross-domain bleed; PROVINCE remains accurate — `.shokunin/lore/PROVINCE.md`; no box checked.

No promotion requested or self-attested.
