# lore — round 6 (coverage axis-move)

Declared before work in `.shokunin/lore/LOG.md`: a cited item transfer must name the prior holder established by an explicit acquisition or preceding transfer; mismatches are reported, never repaired. Baseline report commit `8f56fbdecc0f88db1139410becfc7436ea75f8b1` had no item-provenance rule.

## Work performed
- Added optional item-local `provenance` list with cited initial acquisition and strictly ordered transfers: `.shokunin/lore/corpus/fixtures/check_bible.py`, README and decision table at work commit `19641b286ee4e53f431314e0de37d0b68fe02fbe`. Absent provenance remains accepted; no transfer is inferred from `carries`, narrative, or gameplay.
- Added five-table `item-chain-valid/` and `item-chain-broken/` bibles, identical except final `from_holder`, same work commit. Recorded 12 CLI outputs in `.shokunin/lore/corpus/live/runs/20261012T165220Z/`.
- First-wave reports, executor, non-author reviewer/verifier, correction-bearing verifier report, fresh non-author integrity replay and final adjudicator at `.shokunin/lore/reports/r6-*.md`, all at that work commit. All lanes settled; an integrity-report error was explicitly corrected, not hidden.

## Landed changes
- `.shokunin/lore/LOG.md` declaration, scope clarification and closure; `.shokunin/lore/SCORECARD.md` measured coverage; checker, cited fixtures, run output, reviews, and correction all carried by work commit `19641b286ee4e53f431314e0de37d0b68fe02fbe`. This report lands afterward and cites that hash. No push or merge.

## Before → after measurements
- Baseline `git show 8f56fbdecc0f88db1139410becfc7436ea75f8b1:.shokunin/lore/corpus/fixtures/check_bible.py` has no `provenance` validation. At work commit `19641b286ee4e53f431314e0de37d0b68fe02fbe`, run `python3 .shokunin/lore/corpus/fixtures/check_bible.py .shokunin/lore/corpus/fixtures/<case>`: `item-chain-valid` exit **0**; `item-chain-broken` exit **1** with one `entities[3].provenance[2]` predecessor diagnostic (`harbor` expected, `mira` asserted). Five old fixtures reproduce exact baseline stdout/exit; five round-5 malformed cases retain their errors. Named non-author `lore-r6-independent-verifier` replayed 12 cases and scoped extra probes. Its initial all-files hash claim was withdrawn because the digests differed; `lore-r6-integrity-replay` separately captured equal pre/post hashes of 59 fixture JSON inputs plus checker over five fresh CLI invocations. The later replay proves stability only for its own run.
- **depth: unchanged** — structural chain does not establish canon truth. **coverage: improved** — one explicit item-transfer predecessor class distinguishes paired fixtures. **calibration: unchanged** — bounded limits and corrected hash evidence, but no proof of a gain. Admit: one improved, none harmed. Duplicate-source-ID witness ambiguity, absent textual support for source IDs, unknown intervals, and untested provenance shapes remain limitations.

## SHONEN
- [~] Real decision tables/error patterns/checklists with cited sources — `corpus/knowledge/2026-10-12-lore-decision-table.md`; non-author reviewer `lore-r6-reviewer`, no box checked.
- [~] End-to-end domain task executed and logged — `corpus/live/runs/20261012T165220Z/` and independent verifier/integrity replay; no box checked.
- [~] Instructions executable without oral context — `corpus/fixtures/README.md`, used by verifier; no box checked.
- [~] No cross-domain bleed; PROVINCE remains accurate — `.shokunin/lore/PROVINCE.md` and review; no box checked.

No promotion requested or self-attested.
