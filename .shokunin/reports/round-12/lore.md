# lore — round 12 (calibration axis-move)

Declared in `.shokunin/lore/LOG.md` before dispatch. Baseline report commit `954a1b712590f9b89aed6757e72a8bd4af5c8848` checked occupancy by `(entity_id, tick)` even when multiple valid entity rows shared that actor ID, potentially making an unwarranted **definite** same-actor assertion.

## Work performed
- At work commit `e8724fc944a45f8abc4e5e4be925ae99b7abdd17`, the checker emits field-local `ambiguous actor entity` for each event using a duplicate schema-valid actor ID and skips only occupancy comparison/update for that ID. Raw rows and duplicate-ID finding remain; a unique actor still gets the prior double-booking rule. Dangling actor behavior is unchanged and a known limitation.
- Added fictional pair `corpus/fixtures/r12-{unique-actor,ambiguous-actor}/`, docs/decision table, 26-case run outputs `corpus/live/runs/20261012T175244Z/`, and scoped first-wave/executor/non-author reviewer/verifier/axis reports `reports/r12-*.md`, same work commit. All lanes settled without reported failure.

## Landed changes
- `.shokunin/lore/LOG.md`, `.shokunin/lore/SCORECARD.md`, checker, paired fixtures, bounded docs, saved runs and reports at work commit `e8724fc944a45f8abc4e5e4be925ae99b7abdd17`. This report lands last and cites that hash. No push or merge.

## Before → after and independent evidence
Run `python3 .shokunin/lore/corpus/fixtures/check_bible.py .shokunin/lore/corpus/fixtures/<case>`. Baseline `954a1b7` reported `double-booked 'mira'` for both pair members. Current `r12-unique-actor` still exits 1 with exactly that finding; `r12-ambiguous-actor` exits 1 with duplicate entity ID and two local ambiguous actor references, but no **definite** double-booking. Non-author verifier matched all 24 prior stdout/stderr/exit results byte-for-byte against extracted baseline checker and found 129 JSON hashes unchanged before/after replay. Reviewer probed mixed actor schedules, malformed duplicate rows, same-place ambiguity noise, and the unchanged dangling-actor false-attribution limit. See `reports/r12-independent-verifier.md` and `reports/r12-reviewer.md`.

- **Calibration improved:** unresolved actor identity no longer produces a definite occupancy attribution. Duplicate rows may still describe one actor and a true conflict; the checker does not refute it. Per-row ambiguity adds bounded noise.
- **Coverage unchanged:** no new occupancy rule for a resolved actor or domain class.
- **Depth unchanged:** no new substantiated story. None harmed; admit with those limits. No canon identity, source truth or game-mechanics claim.

## SHONEN
- [~] Real decision tables/error patterns/checklists with cited sources — `corpus/knowledge/2026-10-12-lore-decision-table.md`, `reports/r12-reviewer.md`; no box checked.
- [~] End-to-end domain task executed and logged — `corpus/live/runs/20261012T175244Z/`, `reports/r12-independent-verifier.md`; no box checked.
- [~] Instructions executable without oral context — `corpus/fixtures/README.md`; no box checked.
- [~] No cross-domain bleed; PROVINCE remains accurate — `.shokunin/lore/PROVINCE.md`; no box checked.

No promotion requested or self-attested.
