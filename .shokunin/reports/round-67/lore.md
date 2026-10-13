# lore round 67 — claim citation required field

Work/evidence commit `359087ea4be44b67cd0f913d8dfcdf3c307bde03` by lore-shokunin <lore@shokunin.local>. This report was written afterward. No push or merge.

## Work performed
- `.shokunin/lore/corpus/fixtures/check_bible.py:151` now rejects empty and whitespace-only entity claim `source_id` as a required-field defect even if `sources.json` cannot load; nonempty ID membership remains dependent on the available source index.
- `.shokunin/lore/corpus/fixtures/r67-claim-source-*/` has five matched controls/negatives; `.shokunin/lore/corpus/fixtures/README.md` explains the input-only boundary. `LOG.md` records the declaration, wave plans, critic objection and closure.
- Non-author `reports/r67-reviewer.md` found a second separately repairable claim-field defect; `reports/r67-independent-verifier.md` compared all 125 old fixture raw exit/stdout/stderr tuples (125/125 unchanged), 1,298 original corpus paths (1,296 non-target files unchanged), and all five new CLI cases. Sol `reports/r67-axis-adjudicator.md` independently judged the axes. `git diff --check` and the clean `consistent` CLI were rerun after README section ordering; both succeeded.

## Landed changes and verdict
- Round 67 `LOG.md` closure and checker/fixtures/README landed at `359087ea4be44b67cd0f913d8dfcdf3c307bde03`. **Calibration improved**: blank claim citation reports a claim-local structural repair alongside the source-table loader error, rather than silently evading the field check. **Depth unchanged; coverage unchanged; none harmed. ADMIT.** The global failure already prevented CLEAN, so the gain is diagnostic specificity, not a newly failing bible.
- New CLI: unavailable nonempty control exit 1 loader only; unavailable empty and whitespace each exit 1 loader plus claim-local required-field finding; loaded empty exit 1 claim finding; loaded nonempty control exit 0. Commands and exact raw output are in `reports/r67-independent-verifier.md`. This does not verify source content, fictional truth/canon, rights, or mechanics.

## Before → after measurement
- Before at `262486d`: `python3 .shokunin/lore/corpus/fixtures/check_bible.py <matched empty-claim bible with missing sources.json>` returned only the loader finding, as recorded in `reports/r67-schema-scout.md` and `reports/r67-executor.md`. After `359087ea4be44b67cd0f913d8dfcdf3c307bde03`, run the same command form on `r67-claim-source-unavailable-empty`: loader plus `entities[0].claims[0]: expected nonempty statement and source_id`; whitespace variant likewise. Matched nonempty missing-index control retains only loader error. The new fixture directory changes the path printed in the loader error; it does not alter the field distinction. Old raw tuple replay: 125/125 unchanged, independently verified. No numerical score is used as a verdict.

## SHONEN
- [~] Decision table/error patterns: r67 matched fixture controls and independent verification; no promotion review.
- [~] End-to-end task: non-author reviewer and verifier replayed inputs, Sol adjudicated; no promotion review.
- [~] Executable instructions: checker/README commands verified; no promotion review.
- [~] Province boundary: input claim citation only; no source-text/canon/rights/mechanics claim and no promotion review.
