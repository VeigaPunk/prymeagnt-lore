# lore — round 18 (ambiguous place-ID calibration axis-move)

The falsifiable claim, baseline, lane plan, and post-scout correction were recorded before implementation in `.shokunin/lore/LOG.md`. Baseline report commit `82701ce7680fb062a345e379057c8a097c1539e6` could emit both `ambiguous place entity` and a definite raw-ID `double-booked` for a duplicated place ID.

## Work and lane telemetry
- Work commit `120ef9e88fe0e5c0ab42b4020ec2b2851d0afac9` requires a unique actor and exactly one required-field-screened indexed place entity with `kind == 'place'` for occupied-slot compare/store. All duplicate/ambiguous diagnostics and raw timeline rows remain. Six fixture inputs test a single entity-row paired difference, reverse and mixed-kind duplicates, and known-place pair preservation through ambiguous rows. The corpus docs, LOG/SCORECARD, scout/executor/reviewer/verifier/adjudicator reports, and 45-case raw run `corpus/live/runs/20261012T185657Z/` land in that commit.
- Seven scout reports landed. `lore-r18-test-scout` settled without reply or assigned report; cause unknown, logged in LOG. No test-scout result is claimed. Executor, non-author reviewer and verifier supplied independent replay; final adjudicator wrote `reports/r18-axis-adjudicator.md`.

## Before → after / independent verification
Run `python3 .shokunin/lore/corpus/fixtures/check_bible.py .shokunin/lore/corpus/fixtures/<case>`. `r18-unique-pair` retains the known tower/harbor booking. `r18-duplicate-pair` differs only in one appended complete `harbor` entity row and now retains duplicate/ambiguous findings without definite booking; reversed order and mixed-kind duplicate do likewise. `r18-known-through-ambiguous` and `r18-duplicate-first-known` still report the distinct uniquely indexed tower/quay booking. Non-author verifier: all 194 baseline fixture JSON paths byte-identical at `82701ce`, baseline/current checker stdout/stderr/exit match 39/39 prior fixtures, and current saved outputs match 45/45; reviewer independently replayed 45/45. A malformed excluded duplicate does not increase the screened index count; it is not part of this claim.

## Pareto verdict / bounds
- **Calibration improved**, only for count>1 required-field-screened place IDs: an ambiguous row no longer yields a definite different-uniquely-resolved-places booking, while its ambiguity stays visible.
- **Depth unchanged; coverage unchanged; no harmed axis** on the scoped evidence. The test-only `quay` row is not attested canon. Hidden actual conflict involving an excluded row remains unassessed, not disproved; chosen event orders are not exhaustive pairwise proof. Source IDs and display names do not establish source text, actual place, or story truth.

## Landed changes and SHONEN
Work/LOG/SCORECARD/checker/fixture/knowledge/live evidence landed in `120ef9e88fe0e5c0ab42b4020ec2b2851d0afac9`; **this report lands last**. No push or merge.
- [~] Real decision table and cited review: `corpus/knowledge/2026-10-12-lore-decision-table.md`, `reports/r18-axis-adjudicator.md`; no box checked.
- [~] End-to-end CLI and non-author replay: `corpus/live/runs/20261012T185657Z/`, `reports/r18-independent-verifier.md`; no box checked.
- [~] Runnable instructions: `corpus/fixtures/README.md`; no box checked.
- [~] Province remains `.shokunin/lore/PROVINCE.md`; no cross-domain claim.

No promotion requested or self-attested.
