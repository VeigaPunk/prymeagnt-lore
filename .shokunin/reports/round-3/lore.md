# lore — round 3 (depth axis-move)

Declared before work in `.shokunin/lore/LOG.md` against baseline `ba110ea3495571ce027699dc9bfabc9d2912cffb`: add explicit two-sided cited contradiction records, retain raw assertions, report malformed pointers without choosing canon. Post-scout clarification excludes dangling `missing-map` from a two-sided ledger because no second cited claim exists.

## Work performed
- Added required `contradictions.json` to every example bible (`[]` where no pair is asserted), two source-resolving event-field pairs in `fixtures/contradictions/`, and an unresolved pointer in `fixtures/contradictions-ledger-malformed/`: work commit `23548a66346145696890c62eafd2ea4a01e5a386`.
- Checker validates unique ledger IDs, distinct event-field pointers, allowed fields, unique event targets, their source IDs, and nonempty `why`, without semantic inference: `.shokunin/lore/corpus/fixtures/check_bible.py` at the same commit. README and decision table explain that source resolution is not proof of source support or canon truth.
- First-wave scout/critic reports, executor report, non-author `lore-r3-reviewer`, non-author `lore-r3-independent-verifier`, and final axis adjudicator reports at `.shokunin/lore/reports/r3-*.md` at the same work commit. All lanes settled with no reported failure.

## Landed changes
- `.shokunin/lore/LOG.md` round-3 declaration, post-scout narrowing, and closure; `.shokunin/lore/SCORECARD.md` evidence row; `.shokunin/lore/corpus/**` fixtures/checker/run evidence; all carried by work commit `23548a66346145696890c62eafd2ea4a01e5a386`. This report lands afterward and cites that hash. No push or merge.

## Before → after measurements
- Baseline `git ls-tree -r --name-only ba110ea3495571ce027699dc9bfabc9d2912cffb -- .shokunin/lore/corpus/fixtures/contradictions` lacks `contradictions.json`; checker has only four sections. At work commit `23548a66346145696890c62eafd2ea4a01e5a386`, `python3 .shokunin/lore/corpus/fixtures/check_bible.py .shokunin/lore/corpus/fixtures/<case>`: `consistent` exit **0**; `contradictions` exit **1**, original three reports; `ally-reciprocal` exit **0**; `ally-one-way` exit **1**, original alliance report; `contradictions-ledger-malformed` exit **1** with `contradictions[1].claim_b.event_id` unresolved plus original three. Outputs and exit codes in `.shokunin/lore/corpus/live/runs/20261012T162704Z/`. Non-author verifier compared original four tables and baseline CLI outcomes, tested missing fifth file and malformed reference, and found checker/fixture hashes unchanged after replay.
- **depth: improved** — two explicit editorial claim pairs now resolve to individually cited events. **coverage: unchanged** — no claim of new semantic contradiction class or exhaustive malformed input coverage. **calibration: unchanged** — scope is bounded, but no prior calibration baseline proves movement. Admit: one improved, none harmed. `why` is unchecked editorial text, citations are pointers rather than evidence of source support, and dangling `missing-map` remains outside the ledger.

## SHONEN
- [~] Real decision tables/error patterns/checklists with cited sources — `corpus/knowledge/2026-10-12-lore-decision-table.md`; named non-author reviewer `lore-r3-reviewer` checked scope, no box checked.
- [~] End-to-end domain task executed and logged — `corpus/live/runs/20261012T162704Z/`; `lore-r3-independent-verifier` replayed five cases, no box checked.
- [~] Instructions executable without oral context — `corpus/fixtures/README.md`, used by verifier; no box checked.
- [~] No cross-domain bleed; PROVINCE remains accurate — `.shokunin/lore/PROVINCE.md` and reviewer report; no box checked.

No promotion requested or self-attested.
