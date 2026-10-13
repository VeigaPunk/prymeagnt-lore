# lore round 29 — calibration

Work commit `657da3259de1caab48c6ba8caeaab1baefb1ceec` by lore-shokunin <lore@shokunin.local>. Baseline report commit `5ca92778c86b47bdc06c9cd971a82334c501359f`. This report was written after the work commit. No push/merge.

## Work performed

- Pre-dispatch one-axis claim and eight leaf wave scopes: `.shokunin/lore/LOG.md` round 29 at `657da3259de1caab48c6ba8caeaab1baefb1ceec`. Scoped scout reports `.shokunin/lore/reports/r29-{positive-scout,negative-scout,map-scout,regression-scout,critic,simplifier,scribe,citation-scout}.md`; `r29-map-scout.md` citation placeholder was corrected to line 230 and recorded in LOG before implementation.
- Added new `corpus/fixtures/r29-near-miss/` with five JSON tables identical to r28, one newly authored fictional sentence “The blue seal was near Mira.” and `negative-clause-map.md` marking only `relations[0].type=carries` unsupported by this excerpt, **not false/contradicted** (`reports/r29-executor.md`, `657da3259de1caab48c6ba8caeaab1baefb1ceec`). README documents pair; checker unchanged.
- Named non-author `reports/r29-reviewer.md` traced positive versus negative prose; `reports/r29-independent-verifier.md` replayed old fixtures/bytes; `reports/r29-axis-adjudicator.md` independently replayed and judged each axis. All committed at `657da3259de1caab48c6ba8caeaab1baefb1ceec`.

## Landed changes

- LOG declaration/policy/closure, SCORECARD calibration row, fixture README, seven new fixture files and eleven scoped reports landed at `657da3259de1caab48c6ba8caeaab1baefb1ceec`. This report cites the completed work commit, not its own hash.

## Before → after measurements

- Before baseline `5ca9277`: no r29 fixture path (`git ls-tree -r --name-only 5ca9277 -- .shokunin/lore/corpus/fixtures/r29-near-miss` → empty); r28 map mentions a hypothetical near-miss but no committed negative decision pair. At `657da3259de1caab48c6ba8caeaab1baefb1ceec`, `python3 .shokunin/lore/corpus/fixtures/check_bible.py .shokunin/lore/corpus/fixtures/r28-courier-excerpt` and corresponding `r29-near-miss` both exit 0 with identical CLEAN output, because checker ignores Markdown. Reviewer accepts lexical `carried` conditional on editorial ID alignment; rejects `near` as support for `carries`, but does not infer falsehood. Independent verifier and adjudicator each confirm **79/79** prior stdout/stderr/exit exact, **394/394** old JSON bytes unchanged, and five r29 JSON files identical to r28.
- Per-axis verdict: **calibration improved**, **depth unchanged**, **coverage unchanged**, none harmed (`reports/r29-axis-adjudicator.md`). No canon, source authenticity, rights or other JSON fact is established.

## SHONEN

- [~] Decision table/error patterns: `negative-clause-map.md`, `reports/r29-scribe.md`; no promotion review.
- [~] End-to-end task logged/non-author replayed: `LOG.md` round 29 and `reports/r29-independent-verifier.md`; no SHONEN checkmark review.
- [~] Executable instructions: fixture README round 29; no promotion review.
- [~] Province boundary: `PROVINCE.md` and `reports/r29-citation-scout.md`; no canon, real-world rights or game mechanics; no promotion review.
