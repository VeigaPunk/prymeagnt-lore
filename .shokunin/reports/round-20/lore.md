# lore — round 20 (invalid-tick dependency calibration axis-move)

The claim, baseline and wave plan were declared before dispatch in `.shokunin/lore/LOG.md`. Baseline report commit `47733bfa36216a28c639fd8d5dc891fb4d8de3f5` could call a dependency from tick 0 to an invalid dependent tick -1 a definite inversion while also flagging the tick as negative. The opposite invalid prerequisite orientation silently passed raw order, but was never proof of valid chronology.

## Work and lane telemetry
- Work commit `8923f45498ba12e726d7bfed8ef1b6a985a8a74f` gates only the unique-ID dependency inversion comparison on both endpoint ticks nonnegative. Tick diagnostics, raw rows/IDs, per-edge loop, self/repeated/unknown/ambiguous dependency findings and occupancy remain. Seven input-scoped fixtures, docs, LOG/SCORECARD, eight scout/executor/reviewer/verifier reports, replacement adjudicator report and 56-case raw run `corpus/live/runs/20261012T191902Z/` are included.
- First `lore-r20-axis-adjudicator` child `sub-d9f629f0` exited without reply or assigned report; cause unknown, logged in LOG. It supplied no verdict. Replacement `reports/r20-axis-adjudicator-retry.md` independently adjudicated and admitted narrowly. All other lanes settled with scoped reports.

## Before → after / independent evidence
Run `python3 .shokunin/lore/corpus/fixtures/check_bible.py .shokunin/lore/corpus/fixtures/<case>`. Paired `r20-valid-order` (prereq/dependent `0,1`) is clean; `r20-negative-dependent` differs only in dependent tick (`-1`) and now retains invalid tick but withholds the former raw-tick inversion. `r20-negative-prereq` and `r20-both-negative` retain invalid-tick findings. Valid inversion (`2,1`) and equal (`1,1`) still invert; the equal case also independently double-books at one tick. `r20-mixed-edges` retains a direct valid-to-valid inversion on a dependent that also references an invalid predecessor, establishing selected per-edge preservation. Non-author verifier found 244/244 baseline fixture JSON byte-identical at `47733bf`, 49/49 old stdout/stderr/exit exact baseline/current, 56/56 current saved outputs exact; reviewer and verifier probed self/repeated/unknown/ambiguous findings intact.

## Pareto verdict / bounds
- **Calibration improved** only for negative integer endpoint in a uniquely resolved dependency inversion comparison.
- **Depth unchanged; coverage unchanged; no harmed axis** in scoped evidence. Withholding order does not prove the dependency satisfied, the event absent, or no hidden inversion; valid-to-valid edges remain checked independently. Malformed tick types are screened before indexing; existing malformed dependency-list early skip remains outside this move. Fixture source IDs do not establish source-text chronology, causality or canon.

## Landed changes and SHONEN
Work/LOG/SCORECARD/checker/fixtures/knowledge/live evidence landed in `8923f45498ba12e726d7bfed8ef1b6a985a8a74f`; **this report lands last**. No push or merge.
- [~] Decision table/review: `corpus/knowledge/2026-10-12-lore-decision-table.md`, `reports/r20-axis-adjudicator-retry.md`; no box checked.
- [~] End-to-end CLI/non-author replay: `corpus/live/runs/20261012T191902Z/`, `reports/r20-independent-verifier.md`; no box checked.
- [~] Runnable instructions: `corpus/fixtures/README.md`; no box checked.
- [~] Province remains `.shokunin/lore/PROVINCE.md`; no cross-domain claim.

No promotion requested or self-attested.
