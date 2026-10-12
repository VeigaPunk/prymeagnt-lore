# lore — round 16 (corrected calibration axis-move)

Declared before dispatch in `.shokunin/lore/LOG.md`. Baseline report commit `3995486def3c9fceb95449362f6e8dab8cc130f7` compared raw place-ID strings for a unique actor even when one place ID was missing, causing an unwarranted definite `double-booked` finding alongside the dangling reference.

## Work performed and corrections
- Work commit `64147ca4abbe915b4c3e196cf1a92605b10e73f9` gates occupied-slot comparison/update on a nonzero place-ID count, retaining actor uniqueness and dangling findings. Four fictional fixtures test valid harbor/tower, missing-first, missing-second, and known/missing/known ordering. Bounded docs and 33-case saved CLI outputs `corpus/live/runs/20261012T182817Z/` also land there.
- **First submitted candidate was rejected** by `reports/r16-axis-adjudicator.md`: missing-place descriptions named known Harbor/Tower locations. First prose correction was rejected by `r16-correction-reviewer.md`: “record uses unresolved place ID” risked attributing that key to the cited courier-log. `reports/r16-correction.md` retains both changes and hashes; final descriptions expressly say “Fixture input: Mira's place is unspecified at tick 7.” Fresh non-author `r16-second-correction-reviewer.md` and `r16-second-correction-verifier.md`, then independent `r16-readjudicator.md`, admitted only this second-corrected candidate. All lanes settled without reported failure.

## Landed changes
- `.shokunin/lore/LOG.md`, `.shokunin/lore/SCORECARD.md`, checker, corrected fixture pair/controls, docs/run outputs and all scout/executor/reviewer/verifier/first rejection/correction/readjudication reports at work commit `64147ca4abbe915b4c3e196cf1a92605b10e73f9`. This report lands last. No push or merge.

## Before → after / independent checks
Run `python3 .shokunin/lore/corpus/fixtures/check_bible.py .shokunin/lore/corpus/fixtures/<case>`. At baseline `3995486`, missing `unlisted` in a two-event actor/tick pair yielded dangling **plus** double-booking; now `r16-missing-place` and `r16-missing-first` each exit 1 with dangling only. `r16-valid-places` still reports known harbor/tower conflict; `r16-mixed-three` retains known conflict through missing middle event. The second verifier matched 33/33 current saved outputs, 29/29 prior stdout/stderr/exit against extracted baseline checker, and all 144 baseline JSON paths byte-identical; checker and 164 JSON files were stable across replay. It reconstructed first-correction bytes under current formatting, but initial uncommitted round-16 bytes are not independently recoverable; correction ledger preserves that limit.

- **Calibration improved** for count-zero place ID only; definite conflict involving unresolved location is withheld, not disproven.
- **Coverage unchanged; depth unchanged.** No harmed axis in final candidate. Duplicate/ambiguous and unique wrong-kind place IDs still can feed raw-ID occupancy; selected mixed-three order does not establish general pairwise detection. No source-text or canon proof.

## SHONEN
- [~] Real decision table and cited review at `corpus/knowledge/2026-10-12-lore-decision-table.md`, `reports/r16-readjudicator.md`; no box checked.
- [~] End-to-end CLI run and non-author replay at `corpus/live/runs/20261012T182817Z/`, `reports/r16-second-correction-verifier.md`; no box checked.
- [~] Runnable instructions at `corpus/fixtures/README.md`; no box checked.
- [~] Province remains `.shokunin/lore/PROVINCE.md`; no cross-domain claim or checkmark.

No promotion requested or self-attested.
