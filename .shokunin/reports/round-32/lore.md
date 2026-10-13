# lore round 32 — calibration

Work commit `6e0151a1601663755e29b4ce103d7f1d5ed1175a` by lore-shokunin <lore@shokunin.local>. Baseline report commit `cfaf03a885f36fb6398b5c9dc0810a39cb573807`. This report was written after the work commit. No push/merge.

## Work performed

- Declared a one-axis source-row admission claim and eight leaf wave scopes in `.shokunin/lore/LOG.md` round 32 at `6e0151a1601663755e29b4ce103d7f1d5ed1175a`. Scout reports `.shokunin/lore/reports/r32-{screen-scout,mutation-scout,collateral-scout,regression-scout,critic,simplifier,scribe,citation-scout}.md` distinguished r26's prior entity-row screening from this source-specific case.
- Added `corpus/fixtures/r32-source-malformed/`: copy of r31 admitted duplicate except second raw `courier-log` row's required `title` is `""`; four other tables byte-identical (`reports/r32-executor.md`, `6e0151a1601663755e29b4ce103d7f1d5ed1175a`). Checker unchanged; README warns that raw row still exists.
- Named non-author `reports/r32-reviewer.md` checked triad and admitted counts; `reports/r32-independent-verifier.md` replayed old outputs/bytes; `reports/r32-axis-adjudicator.md` independently checked baseline and judged all axes. All at `6e0151a1601663755e29b4ce103d7f1d5ed1175a`.

## Landed changes

- LOG declaration/policy/closure, SCORECARD calibration row, fixture README, five new JSON files and eleven scoped evidence reports landed at `6e0151a1601663755e29b4ce103d7f1d5ed1175a`. No checker or old JSON edit. This report cites the completed work commit, not itself.

## Before → after measurements

- Before `cfaf03a`: no r32 fixture path (`git ls-tree -r --name-only cfaf03a -- .shokunin/lore/corpus/fixtures/r32-source-malformed` → empty). At `6e0151a1601663755e29b4ce103d7f1d5ed1175a`, `python3 .shokunin/lore/corpus/fixtures/check_bible.py .shokunin/lore/corpus/fixtures/r32-source-malformed` exits 1 with only `sources[2].title: required nonempty str`; no duplicate admitted source-ID nor seven ambiguous reference findings. The unchanged admitted r31 comparator still exits 1 with eight findings; r31 unique exits 0. Named verifier confirmed **83/83** prior stdout/stderr/exit exact and **414/414** old JSON bytes unchanged; adjudicator independently checked using `git archive`.
- Per-axis verdict: **calibration improved**, **depth unchanged**, **coverage unchanged**, none harmed (`reports/r32-axis-adjudicator.md`). Only this checker's admitted source-ID count is demonstrated; raw row remains. No source truth/uniqueness, rights, AI-training permission or canon inference.

## SHONEN

- [~] Decision tables/error patterns: README round 32 and `reports/r32-scribe.md`; no promotion review.
- [~] End-to-end task non-author reviewed/replayed: `LOG.md` round 32, `reports/r32-independent-verifier.md`; no SHONEN checkmark review.
- [~] Executable instructions: fixture README round 32; no promotion review.
- [~] Province boundary: `PROVINCE.md`, `reports/r32-citation-scout.md`; no canon/real-world rights/game mechanics claim; no promotion review.
