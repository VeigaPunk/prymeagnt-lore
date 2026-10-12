# lore — round 4 rejected (coverage move with calibration harm)

Declared before work in `.shokunin/lore/LOG.md`: exact duplicate display names across distinct entity IDs should be reported without merging canon. Baseline report commit `5ceb0e431f686ed0ee29f11b66939c8f661dcc63` had no such check.

## Work performed
- Tested an exact-string name detector and fictional cited fixture pair, then preserved the rejected checker/inputs in `.shokunin/lore/corpus/live/rejected-r4/` at evidence commit `16c0e5a32112100014cf4ffa6e335a85265345cf`. The active checker was restored to its baseline version before this commit.
- Eight scouts/critic/simplifier/scribe, executor, independent reviewer, independent verifier, and axis adjudicator wrote `.shokunin/lore/reports/r4-*.md` at the evidence commit. The non-author verifier confirmed five prior fixture outputs byte-identical to baseline and 25/25 original JSON inputs unchanged; it replayed new pair and targeted probes.
- Filed an unresolved operator choice at `.shokunin/l0-questions.md` because a warning-only mode or sourced opt-in uniqueness convention needs separate adjudication. No operator answer was assumed.

## Landed changes
- `.shokunin/lore/LOG.md` appends declaration, clarification, and rejected closure, carried by evidence commit `16c0e5a32112100014cf4ffa6e335a85265345cf`. `.shokunin/lore/SCORECARD.md` keeps last admitted measurements at round 3. This report lands afterward and cites the evidence commit. No name detector was admitted into the active checker. No push or merge.

## Before → after measurements
- Experimental replay with `python3 .shokunin/lore/corpus/live/rejected-r4/check_bible.py .shokunin/lore/corpus/live/rejected-r4/name-unique` exits **0**; replacing `name-unique` with `name-duplicate` exits **1** with `entities[0]`/`entities[1]` and both IDs. Original seven-case run outputs are in `.shokunin/lore/corpus/live/runs/20261012T163450Z/`; non-author verifier repeated them and verified no file mutation. At evidence commit `16c0e5a32112100014cf4ffa6e335a85265345cf`, `git diff 5ceb0e4 -- .shokunin/lore/corpus/fixtures/check_bible.py` is empty: active checker has no name rule.
- **depth: unchanged** — no new source or identity model. **coverage: improved narrowly in rejected experiment** — exact equal strings detected. **calibration: harmed** — legitimate homonyms cause `VIOLATION` / exit 1 despite review-only text; source metadata does not attest literal names. Admission **denied** because one axis harmed. Do not count the experimental coverage as active capability. See `.shokunin/lore/reports/r4-axis-adjudicator.md`. No verdict was re-rolled.

## SHONEN
- [~] Real decision tables/error patterns/checklists with cited sources — `.shokunin/lore/corpus/knowledge/2026-10-12-lore-decision-table.md` records rejection, non-author reviewer `lore-r4-reviewer`; no box checked.
- [~] End-to-end domain task executed and logged — `.shokunin/lore/corpus/live/runs/20261012T163450Z/` and independent verifier; rejected result, no box checked.
- [~] Instructions executable without oral context — `corpus/fixtures/README.md` points to archived experiment, no box checked.
- [~] No cross-domain bleed; PROVINCE remains accurate — `.shokunin/lore/PROVINCE.md` and no source-rights/game-mechanics claims, no box checked.

No promotion requested. This is an honest rejected round, not a pass.
