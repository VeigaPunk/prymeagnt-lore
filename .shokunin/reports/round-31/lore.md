# lore round 31 — coverage

Work commit `2c6fbbc212bf8d7531849cc33d6ed9b49b6ff1a9` by lore-shokunin <lore@shokunin.local>. Baseline report commit `4da4b949aa03e6595cf9a0d947fb2ba0c44f6fb0`. This report was written after the work commit. No push/merge.

## Work performed

- Pre-dispatch declaration in `.shokunin/lore/LOG.md` round 31 at `2c6fbbc212bf8d7531849cc33d6ed9b49b6ff1a9` explicitly credits r7's ambiguous reverse `allied_with` citation. Eight scout reports `.shokunin/lore/reports/r31-{existing-scout,source-scout,pair-scout,regression-scout,critic,simplifier,scribe,citation-scout}.md` constrained the non-alliance claim.
- Added `corpus/fixtures/r31-source-unique/` (copy of `consistent/`) and `r31-source-ambiguous/` (one extra admitted `courier-log` source row only). The four other tables including `mira -> seal / carries` are byte-identical (`reports/r31-executor.md`, `2c6fbbc212bf8d7531849cc33d6ed9b49b6ff1a9`). README documents full eight-finding fan-out and r7 prior art; checker unchanged.
- Named non-author `reports/r31-reviewer.md` checked pair/r7; `reports/r31-independent-verifier.md` replayed all baseline cases; `reports/r31-axis-adjudicator.md` independently replayed and judged every axis. All at `2c6fbbc212bf8d7531849cc33d6ed9b49b6ff1a9`.

## Landed changes

- LOG declaration/policy/closure, SCORECARD coverage row, README, ten new fixture JSON files and eleven scoped reports landed at `2c6fbbc212bf8d7531849cc33d6ed9b49b6ff1a9`. No checker change or prior JSON edit. This report cites that completed work commit, not itself.

## Before → after measurements

- Before baseline `4da4b94`: no `r31-source-*` fixture paths (`git ls-tree -r --name-only 4da4b94 -- .shokunin/lore/corpus/fixtures/r31-source-unique .shokunin/lore/corpus/fixtures/r31-source-ambiguous` → empty); r7 already tested relation-local source ambiguity on reverse `allied_with`. At `2c6fbbc212bf8d7531849cc33d6ed9b49b6ff1a9`, `python3 .shokunin/lore/corpus/fixtures/check_bible.py .shokunin/lore/corpus/fixtures/r31-source-unique` exits 0 clean; `r31-source-ambiguous` exits 1 with exactly **eight** findings: duplicate source ID, four entity references, one `relations[0].source_id` `carries` reference, and two timeline references. The relation-local finding is one of eight, not sole output. Independent verifier/adjudicator each confirmed **81/81** prior stdout/stderr/exit exact and **404/404** prior JSON bytes unchanged.
- Axis verdict: **coverage improved** narrowly for controlled non-alliance citation input; **depth unchanged**, **calibration unchanged**, none harmed (`reports/r31-axis-adjudicator.md`). No relation truth, source authenticity, canon, rights or training permission claim.

## SHONEN

- [~] Decision tables/error patterns: README round 31 and `reports/r31-scribe.md`; no promotion review.
- [~] End-to-end task and non-author replay: `LOG.md` round 31 and `reports/r31-independent-verifier.md`; no SHONEN checkmark review.
- [~] Executable instructions: fixture README round 31; no promotion review.
- [~] Province boundary: `PROVINCE.md`, `reports/r31-citation-scout.md`; no rights/canon/game mechanics claim; no promotion review.
