# lore — round 7 (calibration axis-move)

Declared before work in `.shokunin/lore/LOG.md`: a duplicated in-world source ID must not qualify as a uniquely resolved citation witness, while both records and original duplicate-ID violation remain. Baseline report commit `4f6eaba9c7f4807b4a28ba9883af5bf479252294` used last-wins source indexing plus membership checks.

## Work performed
- Added shared source-ID count/status for reference sites and alliance witness qualification: `.shokunin/lore/corpus/fixtures/check_bible.py` at work commit `ce8a3578a44b6b309162d26d8bded2bbaa4d7cb2`. Ambiguous ID is reported locally, not called unknown; source rows are untouched. Structural item-chain findings under ambiguous citations are labeled input-structural, not sourced canon.
- Added cited fictional fixture probes `.shokunin/lore/corpus/fixtures/r7-ally-reverse-ambiguous/` and `r7-item-ambiguous/`, README and decision table, with 14-case run output at `corpus/live/runs/20261012T170333Z/`, same work commit.
- Eight first-wave reports, executor, non-author reviewer and verifier, and final axis adjudicator at `.shokunin/lore/reports/r7-*.md`, same work commit. All lanes settled without reported failure.

## Landed changes
- `.shokunin/lore/LOG.md` declaration, qualification policy, verdict; `.shokunin/lore/SCORECARD.md` evidence row; checker, fixtures, documentation and reports in work commit `ce8a3578a44b6b309162d26d8bded2bbaa4d7cb2`. This report lands afterward and cites that hash. No push or merge.

## Before → after measurements
- Baseline `git show 4f6eaba9c7f4807b4a28ba9883af5bf479252294:.shokunin/lore/corpus/fixtures/check_bible.py` qualifies source IDs by membership even after duplicate-ID error. At work commit `ce8a3578a44b6b309162d26d8bded2bbaa4d7cb2`, `python3 .shokunin/lore/corpus/fixtures/check_bible.py .shokunin/lore/corpus/fixtures/<case>`: `r7-ally-reverse-ambiguous` exits **1** with duplicate source, local ambiguous reverse relation, and missing qualified reciprocal; `r7-item-ambiguous` exits **1** with duplicate source and six local ambiguous first-appearance/claim/provenance citations. All 12 prior cases have byte-identical stdout/exit against extracted baseline per non-author `lore-r7-independent-verifier`; 69 fixture JSON files plus checker had equal pre/post hashes during its replay. `lore-r7-reviewer` found a separate uniquely cited reverse edge still qualifies and unrelated duplicate does not create unrelated local reports.
- **depth: unchanged** — no source text or canon-truth model. **coverage: unchanged** — same lore rule classes. **calibration: improved** — ambiguous IDs no longer silently qualify references as uniquely cited. Admit: one improved, none harmed. Multiple local diagnostics may stem from one duplicate ID; unique ID does not prove source support.

## SHONEN
- [~] Real decision tables/error patterns/checklists with cited sources — `corpus/knowledge/2026-10-12-lore-decision-table.md`, non-author reviewer `lore-r7-reviewer`; no box checked.
- [~] End-to-end domain task executed and logged — `corpus/live/runs/20261012T170333Z/` and independent verifier; no box checked.
- [~] Instructions executable without oral context — `corpus/fixtures/README.md`, used by verifier; no box checked.
- [~] No cross-domain bleed; PROVINCE remains accurate — `.shokunin/lore/PROVINCE.md`, no game-mechanics/real-world rights claim; no box checked.

No promotion requested or self-attested.
