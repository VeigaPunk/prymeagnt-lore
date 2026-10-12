# lore — round 11 (calibration axis-move)

Declared in `.shokunin/lore/LOG.md` before dispatch. Baseline report commit `4337c6385ed3f00f45d03eb263028ae313507006` detected duplicate entity IDs yet selected the last duplicate entity row when deciding if a timeline `place_id` was a place. Swapping a valid `harbor` place and character row changed the place-kind finding without changing the referenced ID.

## Work performed
- At work commit `19b73f0ee2dc76784075857083cd7f4a93b8b299`, the checker uses the existing schema-valid entity-ID count at the timeline place-kind branch. More than one matching row gives a local `ambiguous place entity` finding without selecting a kind; one preserves the old place/non-place test; zero preserves dangling. Duplicate-ID findings and rows remain.
- Added fictional order-swapped pair `corpus/fixtures/r11-{place-character,character-place}/`, unique non-place/dangling controls, bounded docs/decision table, 24-case outputs `corpus/live/runs/20261012T174305Z/`, and scoped wave reports `reports/r11-*.md`, same work commit. All lanes settled without reported failure.

## Landed changes
- `.shokunin/lore/LOG.md`, `.shokunin/lore/SCORECARD.md`, checker, pair/controls, docs, run outputs and scout/executor/non-author reviewer/verifier/axis reports at work commit `19b73f0ee2dc76784075857083cd7f4a93b8b299`. This report lands afterward and cites that hash. No push or merge.

## Before → after / verification
Run `python3 .shokunin/lore/corpus/fixtures/check_bible.py .shokunin/lore/corpus/fixtures/<case>`. At baseline `4337c63`, `r11-place-character` reported duplicate `harbor` ID plus `not a place`, but `r11-character-place` reported only duplicate ID. At work commit `19b73f0`, both exit 1 with duplicate-ID and `timeline[0].place_id: ambiguous place entity 'harbor'`; unique non-place remains `not a place 'mira'`, dangling remains `dangling entity 'unlisted'`, unique place stays clean. Non-author verifier extracted baseline checker and compared all 20 prior cases byte-identically in exit/stdout/stderr, captured identical pre/post hash mapping for 119 JSON inputs, and confirmed the pair differs only in row order. Reviewer probed same-kind duplicates, malformed excluded rows and valid homonyms. See `reports/r11-independent-verifier.md`, `reports/r11-reviewer.md`.

- **Calibration improved:** no last-row kind inference for ambiguous timeline places.
- **Coverage unchanged:** no new setting or broader reference class.
- **Depth unchanged:** no new canon facts. None harmed; admit. Only schema-valid entity rows count. This does not validate source text, enforce display-name uniqueness, or resolve other entity references.

## SHONEN
- [~] Real decision tables/error patterns/checklists with cited sources — `corpus/knowledge/2026-10-12-lore-decision-table.md`, `reports/r11-reviewer.md`; no box checked.
- [~] End-to-end domain task executed and logged — `corpus/live/runs/20261012T174305Z/`, `reports/r11-independent-verifier.md`; no box checked.
- [~] Instructions executable without oral context — `corpus/fixtures/README.md`; no box checked.
- [~] No cross-domain bleed; PROVINCE remains accurate — `.shokunin/lore/PROVINCE.md`; no box checked.

No promotion requested or self-attested.
