# lore round 37 — coverage

Work commit `b1a6ed4453e9804e04fd122bfcc92becd1bc1db3` by lore-shokunin <lore@shokunin.local>. Baseline report commit `4e5dacf413d727595aec80ffc1f2e0e2a17f4f84`. This report was written after the work commit. No push/merge.

## Work performed

- Pre-dispatch claim and eight leaf scopes: `.shokunin/lore/LOG.md` round 37 at `b1a6ed4453e9804e04fd122bfcc92becd1bc1db3`. Scout reports `.shokunin/lore/reports/r37-{ledger-scout,duplicate-scout,pair-scout,regression-scout,critic,simplifier,scribe,citation-scout}.md` identified r9's prior generic duplicate/dependency coverage and the distinct ledger-endpoint branch.
- Added r35-derived byte-identical `corpus/fixtures/r37-ledger-unique/` and `r37-ledger-ambiguous/`, the latter adding only an identical copy of `tarin-envelope-observation` at `timeline[4]`. No new source assertion, excerpt edit, ledger edit or checker change (`reports/r37-executor.md`, `b1a6ed4453e9804e04fd122bfcc92becd1bc1db3`). README documents the commands and structural/canon boundary.
- Named non-author `reports/r37-reviewer.md` examined all inherited files, endpoint counts and r9 novelty; `reports/r37-independent-verifier.md` replayed baseline; `reports/r37-axis-adjudicator.md` independently archived/replayed and judged axes. All at `b1a6ed4453e9804e04fd122bfcc92becd1bc1db3`.

## Landed changes and measurements

- LOG declaration/policy/closure, SCORECARD coverage row, README, eighteen new fixture files and twelve scoped reports landed at `b1a6ed4453e9804e04fd122bfcc92becd1bc1db3`; prior JSON/checker unchanged. This report cites the completed work commit, not itself.
- Baseline `4e5dacf`: no r37 fixture (`git ls-tree -r --name-only 4e5dacf -- .shokunin/lore/corpus/fixtures/r37-` → empty). At `b1a6ed4453e9804e04fd122bfcc92becd1bc1db3`, `python3 .shokunin/lore/corpus/fixtures/check_bible.py .shokunin/lore/corpus/fixtures/r37-ledger-unique` exits 0/CLEAN; its `r37-ledger-ambiguous` counterpart exits 1 with exactly `timeline[4].id` duplicate-ID and `contradictions[0].claim_a.event_id` exact-one diagnostics, empty stderr. `claim_a` has two candidates and `claim_b` one. Verifier and adjudicator each found **88/88** old stdout/stderr/exit exact and **439/439** old JSON bytes unchanged.
- Per-axis verdict: **coverage improved** narrowly for two-sided ledger endpoint cardinality beyond r9's generic duplicate/dependency inputs; **depth unchanged**, **calibration unchanged**, none harmed (`reports/r37-axis-adjudicator.md`). The duplicate is an input alias, not a second witness, false testimony or canon resolution. The checker does not validate semantic conflict.

## SHONEN

- [~] Decision table/error patterns: `reports/r37-scribe.md`, fixture README; no promotion review.
- [~] End-to-end task non-author reviewed/replayed: LOG round 37, `reports/r37-independent-verifier.md`; no SHONEN checkmark review.
- [~] Executable instructions: fixture README round 37; no promotion review.
- [~] Province boundary: `PROVINCE.md`, `reports/r37-citation-scout.md`; no canon/real-world rights/game mechanics claim; no promotion review.
