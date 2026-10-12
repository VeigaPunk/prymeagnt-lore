# lore — round 19 (negative-tick occupancy calibration axis-move)

The claim, baseline, and wave plan were declared before dispatch in `.shokunin/lore/LOG.md`. Baseline report commit `9ee1e6eb18b7813a6fe2eda175d891b5d7f55308` emitted a definite `double-booked` at tick -1 while also reporting that both event ticks must be nonnegative.

## Work and independent evidence
- Work commit `05290559442ac4f19ab5da13d72d14d7f4170cd2` adds only `row['tick'] >= 0` to occupied-slot compare/store eligibility. The negative-tick diagnostic, raw row, exact-int screening and dependency inversion remain unchanged. Four input-scoped fixtures include a tick-only negative/valid pair and known-place valid pair through invalid middle or after invalid first. Docs, LOG/SCORECARD, eight scout reports, executor, reviewer, verifier, adjudicator and 49-case raw run `corpus/live/runs/20261012T190807Z/` are included. All lanes settled with scoped reports.
- CLI: `python3 .shokunin/lore/corpus/fixtures/check_bible.py .shokunin/lore/corpus/fixtures/<case>`. `r19-valid-tick` retains tower/harbor booking at tick 9; paired `r19-negative-tick` differs only by both ticks being -1 and now retains two invalid-tick findings without a definite booking. The two mixed-order controls retain valid tick-9 known-place booking. Non-author verifier found 224/224 prior JSON paths byte-identical at baseline `9ee1e6e`, 45/45 prior baseline/current stdout/stderr/exit exact, and 49/49 current saved outputs exact. Reviewer and verifier independently probed unchanged negative-tick dependency inversion.

## Pareto verdict and limits
- **Calibration improved** solely for negative-integer-tick occupancy: a definite occupied-slot assertion is withheld outside the declared nonnegative tick domain.
- **Depth unchanged; coverage unchanged; no harmed axis** on bounded evidence. Negative rows remain indexed and can still participate in raw-tick dependency inversion, a separate unresolved policy. Bool/float ticks fail exact-int required-field screening. Suppression leaves any actual conflict unassessed, not disproved; invalid time does not prove nonoccurrence, source IDs do not establish source text or canon, and tested schedules do not prove exhaustive behavior. Independent `reports/r19-axis-adjudicator.md` admitted narrowly.

## Landed changes and SHONEN
Work/LOG/SCORECARD/checker/fixtures/knowledge/live evidence landed in `05290559442ac4f19ab5da13d72d14d7f4170cd2`; **this report lands last**. No push or merge.
- [~] Decision table/review: `corpus/knowledge/2026-10-12-lore-decision-table.md`, `reports/r19-axis-adjudicator.md`; no box checked.
- [~] End-to-end CLI/non-author replay: `corpus/live/runs/20261012T190807Z/`, `reports/r19-independent-verifier.md`; no box checked.
- [~] Runnable instructions: `corpus/fixtures/README.md`; no box checked.
- [~] Province remains `.shokunin/lore/PROVINCE.md`; no cross-domain claim.

No promotion requested or self-attested.
