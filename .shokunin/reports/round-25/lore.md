# lore round 25 — coverage

Work commit: `0bc30269b07f05dd79eb45d3a217d3027bf1edf4` by lore-shokunin <lore@shokunin.local>. Baseline report commit: `1919faea7a4790244e8dc2cdbb60b652ecfee3c0`. This report was written after the work commit. No push or merge.

## Work performed

- Round-25 declaration and fixture policy preceded dispatch: `.shokunin/lore/LOG.md` at `0bc30269b07f05dd79eb45d3a217d3027bf1edf4`. Eight leaf scout reports `.shokunin/lore/reports/r25-{to-scout,pair-scout,citation-scout,schema-scout,regression-scout,critic,simplifier,scribe}.md` map the missing `to` probe and risks.
- Added matched fixtures `corpus/fixtures/r25-to-unique/` and `r25-to-ambiguous/`: the latter appends only one cited duplicate `seal` entity row, leaving four other JSON tables, including `mira -> seal` and its fictional `courier-log` source ID, byte-identical (`reports/r25-executor.md`). Checker unchanged at `0bc30269b07f05dd79eb45d3a217d3027bf1edf4`.
- Non-author `reports/r25-reviewer.md` checked row admission and citation limits; `reports/r25-independent-verifier.md` replayed the raw cases and all prior fixtures; `reports/r25-axis-adjudicator.md` independently replayed and judged each axis. All are in `.shokunin/lore/reports/` at `0bc30269b07f05dd79eb45d3a217d3027bf1edf4`.

## Landed changes

- The LOG declaration, policy and closure; SCORECARD coverage row; fixture pair and README instructions; eleven scoped reports landed in `0bc30269b07f05dd79eb45d3a217d3027bf1edf4`. No checker source change. This report cites the completed work commit, not its own hash.

## Before → after measurements

- Before: at baseline `1919fae`, no `r25-to-*` fixture paths (`git ls-tree -r --name-only 1919fae -- .shokunin/lore/corpus/fixtures/r25-to-unique .shokunin/lore/corpus/fixtures/r25-to-ambiguous` → empty). After at `0bc30269b07f05dd79eb45d3a217d3027bf1edf4`: `python3 .shokunin/lore/corpus/fixtures/check_bible.py .shokunin/lore/corpus/fixtures/r25-to-unique` exits 0 / zero violations; same command on `r25-to-ambiguous` exits 1 / exactly `entities[4].id: duplicate entities id 'seal'` and `relations[0].to: ambiguous entity 'seal'`; no `from` finding. `reports/r25-independent-verifier.md` found **73/73** old stdout/stderr/exit results exact and **364/364** old JSON paths byte-identical, plus ten new JSON paths. Adjudicator independently confirmed.
- Per-axis verdict: **coverage improved**, **depth unchanged**, **calibration unchanged**, none harmed (`reports/r25-axis-adjudicator.md`). Admit narrowly: proves structural `to`-endpoint diagnostic position, not source-text truth, existence of a second canonical seal, or the relation's truth.

## SHONEN

- [~] Decision table/checklist: `corpus/fixtures/README.md` rounds 24–25; no promotion review.
- [~] End-to-end task executed: `LOG.md` round 25, named non-author `reports/r25-independent-verifier.md`; no SHONEN checkmark review.
- [~] Executable instructions: `corpus/fixtures/README.md` command pair; no promotion review.
- [~] Province boundary: `PROVINCE.md`, `reports/r25-citation-scout.md`, in-world ID versus canon limitations; no promotion review.
