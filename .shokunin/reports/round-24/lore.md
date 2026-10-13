# lore round 24 — coverage

Work commit: `cc2b73a2227326746aa80d05cd5cc7e5676d7855` (lore-shokunin <lore@shokunin.local>). Baseline: `d0e1c73b28fdf971c41cb095d709bfcd9edeffbc`. Branch: `craft/lore-r1`. Report written after work commit; no push or merge.

## Work performed

- Declared one coverage claim and two explicit pre-implementation test corrections in `.shokunin/lore/LOG.md`, round 24, at `cc2b73a2227326746aa80d05cd5cc7e5676d7855`. The checked-out branch already closed rounds 2–23, superseding the mission brief’s stale round-1-only premise.
- Eight leaf scouts mapped the rule, fixtures, citation boundary and risks at `.shokunin/lore/reports/r24-{index-scout,schema-scout,fixture-scout,regression-scout,citation-scout,critic,simplifier,scribe}.md`, committed at `cc2b73a2227326746aa80d05cd5cc7e5676d7855`; scoped executor’s code and results are in `r24-executor.md`.
- Added one relation-local ambiguity diagnostic to `.shokunin/lore/corpus/fixtures/check_bible.py` and the bounded endpoint decision table to `corpus/fixtures/README.md`, both in `cc2b73a2227326746aa80d05cd5cc7e5676d7855`. No fixture JSON changed; no duplicate row is chosen.
- Non-author `r24-reviewer.md` inspected count/precedence/canon limits. Non-author `r24-independent-verifier.md` replayed all 73 existing fixtures against the baseline checker and compared stdout, stderr, and exit; `r24-axis-adjudicator.md` independently replayed and gave per-axis verdicts. All reports in `.shokunin/lore/reports/` at `cc2b73a2227326746aa80d05cd5cc7e5676d7855`.

## Landed changes

- The round-24 LOG declaration/corrections/closure and `.shokunin/lore/SCORECARD.md` coverage row, plus the checker, README, and eleven scoped evidence reports, landed in `cc2b73a2227326746aa80d05cd5cc7e5676d7855`. The LOG closure cites the non-author verifier and adjudicator; this report cites the completed work commit rather than itself.

## Before → after measurements

- Command: `python3 .shokunin/lore/corpus/fixtures/check_bible.py .shokunin/lore/corpus/fixtures/r12-ambiguous-actor`. At baseline `d0e1c73`, exit 1 / 3 violations without relation-local ambiguity. At `cc2b73a2227326746aa80d05cd5cc7e5676d7855`, exit 1 / 4 violations including `VIOLATION: relations[0].from: ambiguous entity 'mira'`; no other prior finding changes. `r21-ambiguous-actor` similarly changes 4→5. Independent replay: 73/73 executed; only these two add that line and +1 total; other 71 exact; 364/364 pre-existing fixture JSON paths byte-identical (`r24-independent-verifier.md`). `consistent/` exits 0. `r12-unique-actor` stays exit 1 for its pre-existing occupancy conflict and has no endpoint ambiguity; it is not a clean-bible control.
- Axis verdicts from `r24-axis-adjudicator.md`: **coverage improved**, **depth unchanged**, **calibration unchanged**; none harmed. Admitted narrowly. Duplicate `to` endpoint has no separate fixture probe; no source-text truth, chronology or canon claim follows.

## SHONEN

- [~] Decision tables/error patterns with cited sources: `corpus/fixtures/README.md` round-24 table and `reports/r24-reviewer.md`; no promotion review.
- [~] End-to-end domain task executed and logged: `LOG.md` round 24 and `reports/r24-independent-verifier.md` (named non-author); no SHONEN checkmark review.
- [~] Instructions executable without oral context: `corpus/fixtures/README.md` command and verdict scope; no promotion review.
- [~] No cross-domain bleed: `PROVINCE.md`, in-world citation boundary in README, `reports/r24-citation-scout.md`; no promotion review.
