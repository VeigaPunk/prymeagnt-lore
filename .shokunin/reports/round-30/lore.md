# lore round 30 — calibration

Work commit `635f8b6a91ed408f067a58a8fbff51388c49c568` by lore-shokunin <lore@shokunin.local>. Baseline report commit `533e36712a3acefe7aa2ccb7e03f44aeb20efdbd`. This report was written after the work commit. No push/merge.

## Work performed

- Round-30 claim and wave plan preceded dispatch: `.shokunin/lore/LOG.md` at `635f8b6a91ed408f067a58a8fbff51388c49c568`. Seven wave-1 scout reports `.shokunin/lore/reports/r30-{negation-scout,triad-scout,map-scout,regression-scout,critic,scribe,citation-scout}.md` landed. The eighth `lore-r30-simplifier` child `sub-06bec5e3` exited with no reply/report; LOG records failure and it supplied no evidence.
- Added `corpus/fixtures/r30-explicit-negation/` with five unchanged JSON tables, newly authored fictional “I, Mira, did not carry the blue seal.” and a manual conditional textual-conflict map for only `relations[0].type=carries` (`reports/r30-executor.md`, `635f8b6a91ed408f067a58a8fbff51388c49c568`). README preserves same-proposition/occasion and no-canon bounds; checker unchanged.
- Non-author `reports/r30-reviewer.md` independently classified the r28/r29/r30 prose triad. `reports/r30-independent-verifier.md` reported 80/399 replay but referenced an uncommitted `/tmp/r30check.py`; `reports/r30-axis-adjudicator.md` independently reran using `git archive`, same fixture argv for both checkers (avoiding an absolute-path diagnostic difference), and judged axes. All at `635f8b6a91ed408f067a58a8fbff51388c49c568`.

## Landed changes

- LOG declaration/telemetry/closure, SCORECARD calibration row, fixture README, seven new fixture files and ten scoped reports landed at `635f8b6a91ed408f067a58a8fbff51388c49c568`; the failed scout report is **absent**. No checker or old JSON edit. This report cites the completed work commit, not itself.

## Before → after measurements

- Before `533e367`: no r30 fixture (`git ls-tree -r --name-only 533e367 -- .shokunin/lore/corpus/fixtures/r30-explicit-negation` → empty); r28 constructed positive and r29 unsupported proximity had no explicit denial case. At `635f8b6a91ed408f067a58a8fbff51388c49c568`, `python3 .shokunin/lore/corpus/fixtures/check_bible.py .shokunin/lore/corpus/fixtures/r30-explicit-negation` exits 0 / exact CLEAN output, like r28 and r29, because prose is not parsed. Human review distinguishes conditional lexical support, unsupported proximity, and explicit textual conflict **only if IDs and occasion align**. Final adjudicator independently found **80/80** old stdout/stderr/exit exact on same fixture argv and **399/399** prior JSON bytes unchanged; five new JSON tables match r28/r29.
- Per-axis verdict: **calibration improved**, **depth unchanged**, **coverage unchanged**, none harmed (`reports/r30-axis-adjudicator.md`). No claim of canon falsity, all-time non-carrying, source authenticity, rights or other JSON truth.

## SHONEN

- [~] Decision table/error patterns: `textual-conflict-map.md`, `reports/r30-scribe.md`; no promotion review.
- [~] End-to-end task non-author reviewed/replayed: `LOG.md` round 30, `reports/r30-reviewer.md`, `reports/r30-axis-adjudicator.md`; no SHONEN checkmark review.
- [~] Executable instructions: fixture README round 30; no promotion review.
- [~] Province boundary: `PROVINCE.md` and `reports/r30-citation-scout.md`; no canon, real-world rights or game mechanics; no promotion review.
