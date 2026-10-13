# lore round 34 — calibration

Work commit `2932b5fc3b50568dca1fd043ce23f591b498061e` by lore-shokunin <lore@shokunin.local>. Baseline report commit `e717c7430db82b46c8aa9255dbf78504c770ca59`. This report was written after the work commit. No push/merge.

## Work performed

- Pre-dispatch one-axis declaration and eight leaf scopes: `.shokunin/lore/LOG.md` round 34 at `2932b5fc3b50568dca1fd043ce23f591b498061e`. Scout reports `.shokunin/lore/reports/r34-{modality-scout,record-scout,pair-scout,regression-scout,critic,simplifier,scribe,citation-scout}.md` identify the evidence-modality distinction.
- Added `corpus/fixtures/r34-tarin-hearsay/` with five JSON files byte-identical to r33, newly authored “I, Tarin, heard that Sella placed...” excerpt and `modality-contrast-map.md` marking unchanged `reports seeing` fields unsupported by **this** excerpt as direct sight, not false (`reports/r34-executor.md`, `2932b5fc3b50568dca1fd043ce23f591b498061e`). README describes checker/prose separation; checker unchanged.
- Named non-author `reports/r34-reviewer.md` classified r33 direct-sighting report vs r34 hearsay report; `reports/r34-independent-verifier.md` replayed old fixtures; `reports/r34-axis-adjudicator.md` independently used `git archive` and judged axes. All at `2932b5fc3b50568dca1fd043ce23f591b498061e`.

## Landed changes

- LOG declaration/policy/closure, SCORECARD calibration row, fixture README, seven new fixture artifacts and eleven scoped reports landed in `2932b5fc3b50568dca1fd043ce23f591b498061e`. No checker/old JSON edit. This report cites the completed work commit, not itself.

## Before → after measurements

- Baseline `e717c74`: no r34 fixture (`git ls-tree -r --name-only e717c74 -- .shokunin/lore/corpus/fixtures/r34-tarin-hearsay` → empty); r33 authored “saw” with matching report fields. At `2932b5fc3b50568dca1fd043ce23f591b498061e`, `python3 .shokunin/lore/corpus/fixtures/check_bible.py .shokunin/lore/corpus/fixtures/r33-tarin-envelope` and corresponding `r34-tarin-hearsay` both exit 0 / exact CLEAN output. Five JSON files match byte-for-byte, yet r34 “heard that” does not support unchanged direct-sight fields; Sella placement remains an attributed hearsay claim, neither verified nor false. Independent verifier/adjudicator each found **85/85** old stdout/stderr/exit exact and **424/424** old JSON bytes unchanged.
- Axis verdict: **calibration improved**, **depth unchanged**, **coverage unchanged**, none harmed (`reports/r34-axis-adjudicator.md`). No informant, event truth, envelope content, source authenticity or canon claim.

## SHONEN

- [~] Decision table/error patterns: `modality-contrast-map.md`, `reports/r34-scribe.md`; no promotion review.
- [~] End-to-end task non-author reviewed/replayed: LOG round 34, `reports/r34-independent-verifier.md`; no SHONEN checkmark review.
- [~] Executable instructions: fixture README round 34; no promotion review.
- [~] Province boundary: `PROVINCE.md`, `reports/r34-citation-scout.md`; no canon/real-world rights/game mechanics claim; no promotion review.
