# lore — round 17 (wrong-kind place calibration axis-move)

The falsifiable claim, baseline and lane plan were declared before dispatch in `.shokunin/lore/LOG.md`. Baseline report commit `1dd6f27ae89a096c8fb99d2750f35e5118fda5d3` emitted both `not a place` and a definite raw-ID `double-booked` for unique character `mira` used as a place at the same actor/tick as valid `harbor`.

## Work and lane telemetry
- Work commit `7cb6ae78bb9cbc438f671169e2726d0015106750` adds a narrow checker guard excluding exactly one indexed non-place entity ID from occupancy compare/store, without changing the diagnostic. Six input-scoped fixtures test a paired valid/wrong-kind `place_id`, reverse order, and wrong-kind first/middle/last around known places. Docs, scout/executor/reviewer/verifier/adjudicator reports and 39-case raw run `corpus/live/runs/20261012T184609Z/` are included.
- Eight scout leaves, executor, reviewer, verifier and replacement adjudicator settled without reported failures. The **first** independent adjudicator child `sub-e4bf535a` exited without reply or assigned report; cause unknown, logged in LOG. It supplied no verdict. Replacement `r17-axis-adjudicator-retry.md` independently reviewed and admitted narrowly; no outcome is imputed to the failed lane.

## Before → after and independent replay
Command: `python3 .shokunin/lore/corpus/fixtures/check_bible.py .shokunin/lore/corpus/fixtures/<case>`. `r17-valid-places` reports harbor/tower `double-booked` while paired `r17-wrong-after` differs only in second-row `place_id` (`tower` → `mira`) and now reports `not a place` only; baseline reported an unsupported raw-ID booking as well. `r17-wrong-before` reports wrong-kind only. `r17-wrong-{first,middle,last}` retain the known harbor/tower finding while withholding comparisons involving wrong-kind `mira`. Non-author verifier: all 164 baseline fixture JSON paths byte-identical to report commit `1dd6f27`, baseline/current checker stdout/stderr/exit match 33/33 prior fixtures, and current saved outputs match 39/39; 194 JSON plus checker stable during replay. Reviewer also probed unknown nonempty kind (indexed, unknown-kind and not-a-place diagnostics, excluded) and missing kind (screened out, dangling).

## Pareto verdict / bounds
- **Calibration improved**, exactly for count-one indexed wrong-kind place IDs: retain the kind finding and withhold a definite different-resolved-place comparison involving that row.
- **Depth unchanged; coverage unchanged; no harmed axis** in the admitted scoped candidate. Duplicate/ambiguous place IDs still participate in raw-ID occupancy despite ambiguity; the older `r11-unique-nonplace` prose names harbor when its raw place ID is `mira`, so it was not used as evidence. A hidden true conflict involving an excluded row remains unassessed. Tested orders are not general pairwise completeness. Unique source IDs and fixture descriptions do not establish source text, actual location, or canon.

## Landed changes and SHONEN
All work/LOG/SCORECARD/fixture/checker/knowledge/live evidence landed in `7cb6ae78bb9cbc438f671169e2726d0015106750`; **this report lands last**. No push or merge.
- [~] Real decision table and cited review: `corpus/knowledge/2026-10-12-lore-decision-table.md`, `reports/r17-axis-adjudicator-retry.md`; no box checked.
- [~] End-to-end CLI and independent replay: `corpus/live/runs/20261012T184609Z/`, `reports/r17-independent-verifier.md`; no box checked.
- [~] Runnable instructions: `corpus/fixtures/README.md`; no box checked.
- [~] Province remains `.shokunin/lore/PROVINCE.md`; no cross-domain claim.

No promotion requested or self-attested.
