# lore — round 22 (mixed dependency-list coverage move; operator pause)

The claim, baseline, wave plan and diagnostic policy were declared before implementation in `.shokunin/lore/LOG.md`. Baseline report commit `cc92ecee56fa771d7344df9e85e9c1ce2146be3a` reported one malformed-list error and skipped all string siblings, masking an otherwise inspectable dependency inversion.

## Work and independent evidence
- Work commit `8ed2090126737f3271c401ce4791bc0048481057` retains one row-level `expected event-id strings` diagnostic before member findings, skips each non-string before ID/set lookup, and checks string siblings in their original order under existing self/repeated/unknown/ambiguous/tick-valid inversion semantics. Occupancy is unchanged. Eight input-scoped fixtures, docs, LOG/SCORECARD, eight scout reports, executor/reviewer/verifier/adjudicator and 72-case raw run `corpus/live/runs/20261012T193930Z/` land there. All lanes settled with reports.
- CLI: `python3 .shokunin/lore/corpus/fixtures/check_bible.py .shokunin/lore/corpus/fixtures/<case>`. Paired `r22-clean-inversion` versus `r22-mixed-last` differs only by added `null`; both report inversion, mixed also reports the malformed-list finding. `r22-mixed-first`, multiple unhashable values, unknown/self/repeated and ordered/only-malformed controls bound the behavior. Non-author verifier found 319/319 prior fixture JSON paths byte-identical at `cc92ece`, baseline/current stdout/stderr/exit same 64/64 old cases, and current saved outputs exact 72/72. Independent `reports/r22-axis-adjudicator.md` replayed and admitted narrowly.

## Pareto verdict / bounds
- **Coverage improved** only for safe string-member findings formerly masked by a malformed sibling.
- **Depth unchanged; calibration unchanged; no harmed axis** in bounded evidence. One malformed member and any edge it purports to encode remain unassessed, not satisfied. Fixture fields and citation IDs do not establish source-text chronology, event occurrence, causality or canon. No broad malformed-input guarantee follows.

## Landed changes, SHONEN and pause
Work/LOG/SCORECARD/checker/fixtures/knowledge/live evidence landed in `8ed2090126737f3271c401ce4791bc0048481057`; **this report lands last**. No push or merge.
- [~] Decision table/review: `corpus/knowledge/2026-10-12-lore-decision-table.md`, `reports/r22-axis-adjudicator.md`; no box checked.
- [~] End-to-end CLI/non-author replay: `corpus/live/runs/20261012T193930Z/`, `reports/r22-independent-verifier.md`; no box checked.
- [~] Runnable instructions: `corpus/fixtures/README.md`; no box checked.
- [~] Province remains `.shokunin/lore/PROVINCE.md`; no cross-domain claim.

No promotion requested or self-attested. Operator pause is recorded verbatim in LOG; **no round 23**.
