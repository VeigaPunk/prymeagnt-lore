# lore — round 21 (malformed dependency masking occupancy coverage move)

The claim, baseline and wave plan were declared before dispatch in `.shokunin/lore/LOG.md`. Baseline report commit `64d2673fb87ffb25396948840a991ee88472f8bf` let a non-string dependency member trigger an early row `continue`, masking an independent same-actor/tick booking at distinct uniquely indexed places.

## Work and independent evidence
- Work commit `fa98378506f560b0a756d0bbc7b97820291f1d8b` moves only the existing guarded occupancy compare/store before the malformed dependency-list early exit. The `expected event-id strings` finding remains, and all member-wise dependency checks still skip a malformed list. Eight input-scoped fixtures, docs, LOG/SCORECARD, eight scout reports, executor/reviewer/verifier/adjudicator and 64-case raw run `corpus/live/runs/20261012T193022Z/` are included. All lanes settled with reports.
- CLI: `python3 .shokunin/lore/corpus/fixtures/check_bible.py .shokunin/lore/corpus/fixtures/<case>`. Paired `r21-clean` and `r21-malformed` differ only by second-row `depends_on: []` versus `[null]`; both now report known-place booking, malformed also reports type error. Reverse place-order pair repeats the result. Same-place, invalid-tick, wrong-kind-place, and ambiguous-actor controls gain no booking. Non-author verifier found 279/279 prior fixture JSON paths byte-identical at `64d2673`, baseline/current stdout/stderr/exit identical 56/56 old cases, current saved outputs exact 64/64; malformed-first and mixed-string/null temporary probes retain slot insertion and list-wide skip.

## Pareto verdict / bounds
- **Coverage improved** only for otherwise-definite occupancy formerly masked by a non-string dependency member.
- **Depth unchanged; calibration unchanged; no harmed axis** on bounded evidence. The checker does not recover valid dependency members from a mixed malformed list; those lookups remain unassessed, not satisfied. Actor/place/tick certainty guards are unchanged. Fixture fields, citation IDs and checker findings do not establish source text, event occurrence or canon. Independent `reports/r21-axis-adjudicator.md` admitted narrowly.

## Landed changes and SHONEN
Work/LOG/SCORECARD/checker/fixtures/knowledge/live evidence landed in `fa98378506f560b0a756d0bbc7b97820291f1d8b`; **this report lands last**. No push or merge.
- [~] Decision table/review: `corpus/knowledge/2026-10-12-lore-decision-table.md`, `reports/r21-axis-adjudicator.md`; no box checked.
- [~] End-to-end CLI/non-author replay: `corpus/live/runs/20261012T193022Z/`, `reports/r21-independent-verifier.md`; no box checked.
- [~] Runnable instructions: `corpus/fixtures/README.md`; no box checked.
- [~] Province remains `.shokunin/lore/PROVINCE.md`; no cross-domain claim.

No promotion requested or self-attested.
