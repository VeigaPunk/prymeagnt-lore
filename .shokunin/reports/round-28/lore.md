# lore round 28 — depth

Work commit `c86d7a5a3f0dd31d28ec783a02c81446de88b8f0` by lore-shokunin <lore@shokunin.local>. Baseline report commit `aaa8d724f5820b07a5cb2d498777306763001441`. This report was written after the work commit. No push/merge.

## Work performed

- Declared one depth move and planned eight scoped leaf scouts before dispatch in `.shokunin/lore/LOG.md` round 28 at `c86d7a5a3f0dd31d28ec783a02c81446de88b8f0`. Scout reports `.shokunin/lore/reports/r28-{source-scout,clause-scout,map-scout,regression-scout,critic,simplifier,scribe,citation-scout}.md` bound the clause and risks.
- Added separate `corpus/fixtures/r28-courier-excerpt/`, five JSON files byte-identical to `consistent/`, newly authored fictional `courier-log-excerpt.md` (“I, Mira, carried the blue seal.”), and `relation-clause-map.md` for only `relations[0]`. Map separates lexical `carried` from editorial ID alignment; checker does not read Markdown (`reports/r28-executor.md`, `c86d7a5a3f0dd31d28ec783a02c81446de88b8f0`). README describes limits.
- Non-author `reports/r28-reviewer.md` traced clause and rejected “the seal was near Mira” as `carries`. `reports/r28-independent-verifier.md` supplied 78/389 replay evidence despite no explicit reply; its displayed exclusion typo was corrected and logged before final judgment. `reports/r28-axis-adjudicator.md` independently repeated full baseline replay and judged axes. All reports at `c86d7a5a3f0dd31d28ec783a02c81446de88b8f0`.

## Landed changes

- LOG declaration/corrections/closure, SCORECARD depth row, fixture README, seven new fixture files and eleven scoped reports in `c86d7a5a3f0dd31d28ec783a02c81446de88b8f0`. No checker algorithm or prior JSON edit. This report cites the completed work commit, not itself.

## Before → after measurements

- Baseline `aaa8d72`: no r28 fixture path (`git ls-tree -r --name-only aaa8d72 -- .shokunin/lore/corpus/fixtures/r28-courier-excerpt` → empty), no corresponding manual relation clause map. At `c86d7a5a3f0dd31d28ec783a02c81446de88b8f0`, `python3 .shokunin/lore/corpus/fixtures/check_bible.py .shokunin/lore/corpus/fixtures/r28-courier-excerpt` exits 0 / `CLEAN: schema, citations, relations, timeline; 0 violations`; this **does not** test prose. Named reviewer traced actor/action/object against the single excerpt and rejected a proximity near-miss. Final adjudicator independently found 78/78 prior stdout/stderr/exit exact, 389/389 old JSON bytes unchanged, five new JSON tables equal `consistent/`.
- Per-axis verdict: **depth improved**, **coverage unchanged**, **calibration unchanged**, none harmed (`reports/r28-axis-adjudicator.md`). Improvement is manual inspectability of one constructed clause, not source authenticity, extra canon, or evidence for other copied JSON claims/events.

## SHONEN

- [~] Decision tables/checklists: manual clause map and `reports/r28-reviewer.md`; no promotion review.
- [~] End-to-end task logged and non-author reviewed: `LOG.md` round 28, `reports/r28-independent-verifier.md`; no SHONEN checkmark review.
- [~] Executable instructions: fixture README round 28; no promotion review.
- [~] Province boundary: `PROVINCE.md` and `reports/r28-citation-scout.md`; no canon, real-world rights or game-mechanics claim; no promotion review.
