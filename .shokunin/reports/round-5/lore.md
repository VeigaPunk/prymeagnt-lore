# lore — round 5 (calibration axis-move)

Declared before work in `.shokunin/lore/LOG.md`: measure CLI error patterns on isolated malformed bibles, independently replay each row, and leave checker behavior unchanged. Baseline report `b6ca1e902f2bf08b8acddaef665d9764f8636981` lacked the measured decision table; the round-4 exact-name detector was rejected and remains inactive.

## Work performed
- Added five raw single-mutation fixture siblings `corpus/fixtures/r5-{missing-file,invalid-json,wrong-top-level,row-shape,invalid-citation}/` and a six-row measured decision table `corpus/knowledge/2026-10-12-malformed-error-patterns.md` at work commit `1d1bf0693376c0635a759de870f914fccc7973d4`. Clean control is existing `corpus/fixtures/consistent/`.
- Preserved stdout/exit status for six matrix cases and four regressions at `.shokunin/lore/corpus/live/runs/20261012T164316Z/`, same work commit. No new checker rule; `git diff --exit-code b6ca1e9 -- .shokunin/lore/corpus/fixtures/check_bible.py` has no diff.
- Eight first-wave leaf reports, executor replay protocol, non-author `lore-r5-reviewer` and `lore-r5-independent-verifier`, and final axis adjudicator reside under `.shokunin/lore/reports/r5-*.md`, same work commit. All lanes settled without reported failure.

## Landed changes
- `.shokunin/lore/LOG.md` declaration and verdict; `.shokunin/lore/SCORECARD.md` calibration measurement; raw fixtures, table, replay evidence, and lane reports, all carried by work commit `1d1bf0693376c0635a759de870f914fccc7973d4`. This report lands afterward and cites the work hash. No push or merge.

## Before → after measurements
- Baseline `git ls-tree -r --name-only b6ca1e902f2bf08b8acddaef665d9764f8636981 -- .shokunin/lore/corpus/fixtures/r5-*` returns no cases; baseline lacks `corpus/knowledge/2026-10-12-malformed-error-patterns.md`. At work commit `1d1bf0693376c0635a759de870f914fccc7973d4`, run `python3 .shokunin/lore/corpus/fixtures/check_bible.py .shokunin/lore/corpus/fixtures/<case>`: `consistent` exits **0**; each `r5-*` exits **1** with respectively missing-file `cannot load JSON`, parse-error `cannot load JSON`, `expected array`, `expected object`, and `unknown in-world source`; only one violation in these low-cascade cases. Exact outputs in `corpus/live/runs/20261012T164316Z/`. Independent verifier replayed all six plus four prior fixtures, compared one-path mutations, found unchanged checker SHA-256 `0008496a65e6e0696b638a081c78c44cf4e323d7f56441a6105631ecc689769d` and unchanged hashes for 49 present JSON inputs.
- **depth: unchanged** — no richer lore model. **coverage: unchanged** — checker bytes/rules unchanged. **calibration: improved** — a bounded table of observed error classes is reproducible and independently verified where baseline had none. Admit: one improved, none harmed. Missing/invalid JSON share a class but have distinct causes; OS/parser suffixes vary. One mutated file may cascade in other examples, and these samples are not exhaustive.

## SHONEN
- [~] Real decision tables/error patterns/checklists with cited sources — `corpus/knowledge/2026-10-12-malformed-error-patterns.md`, independently checked by `lore-r5-independent-verifier`; no box checked.
- [~] End-to-end domain task executed and logged — `corpus/live/runs/20261012T164316Z/` and verifier replay; no box checked.
- [~] Instructions executable without oral context — `corpus/fixtures/README.md` and `reports/r5-executor.md`; no box checked.
- [~] No cross-domain bleed; PROVINCE remains accurate — `.shokunin/lore/PROVINCE.md`, no game-mechanics or real-world permission assertions; no box checked.

No promotion requested or self-attested.
