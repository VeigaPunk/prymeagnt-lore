# lore — round 8 (coverage axis-move)

Declared before work in `.shokunin/lore/LOG.md`: report repeated prerequisite IDs and explicit self-dependency within a cited event's list, retaining the prior tick-inversion check. Baseline report commit `17736ae5ed260c4b99f98efd9b194254ccd2aa87` accepted a repeated *earlier* prerequisite; self already failed as equal-tick inversion.

## Work performed
- Added list-local repeat and self diagnostics without changing raw events or source IDs; repeated IDs now run existing target/tick lookup once, while self keeps its old inversion diagnostic: `.shokunin/lore/corpus/fixtures/check_bible.py` at work commit `d7461ed1ef45cac9b248e0d576e6628306bdb542`.
- Added cited fictional sibling fixtures `.shokunin/lore/corpus/fixtures/r8-deps-{distinct,anomalous}/`, README and decision-table scope, and 16-case run evidence `corpus/live/runs/20261012T171326Z/`, same commit.
- Eight first-wave reports, executor, non-author reviewer, non-author verifier and final axis adjudicator at `.shokunin/lore/reports/r8-*.md`, same work commit. All lanes settled without reported failure.

## Landed changes
- `.shokunin/lore/LOG.md` declaration, post-scout narrowing and closure; `.shokunin/lore/SCORECARD.md` measurement; checker, fixtures, docs, runs and reports at work commit `d7461ed1ef45cac9b248e0d576e6628306bdb542`. This report lands afterward and cites that hash. No push or merge.

## Before → after measurements
- Baseline `git show 17736ae5ed260c4b99f98efd9b194254ccd2aa87:.shokunin/lore/corpus/fixtures/check_bible.py` checks each dependency's ID/tick but not repeated membership. At work commit `d7461ed1ef45cac9b248e0d576e6628306bdb542`, run `python3 .shokunin/lore/corpus/fixtures/check_bible.py .shokunin/lore/corpus/fixtures/<case>`: `r8-deps-distinct` exits **0**; `r8-deps-anomalous` exits **1** with repeat at `timeline[1].depends_on[1]`, self at `[2]`, and baseline self inversion. Non-author verifier isolated `['departure','departure']`: exit 1 with only repeat finding, proving newly detected case; self-only still yields self plus old inversion. All 14 pre-round cases matched baseline stdout/stderr/exit byte-for-byte; verifier found equal pre/post hashes for checker and 79 JSON inputs. Full output `corpus/live/runs/20261012T171326Z/`.
- **depth: unchanged** — no new lore or causal model. **coverage: improved** — duplicate earlier prerequisite no longer silently accepted. **calibration: unchanged** — self is diagnostic clarity, not new detection; duplicate event-ID lookup remains last-wins/order-dependent. Admit: one improved, none harmed. This is list integrity, not proof that cited sources support dependencies or a graph-cycle check.

## SHONEN
- [~] Real decision tables/error patterns/checklists with cited sources — `corpus/knowledge/2026-10-12-lore-decision-table.md`, non-author reviewer `lore-r8-reviewer`; no box checked.
- [~] End-to-end domain task executed and logged — `corpus/live/runs/20261012T171326Z/` and verifier; no box checked.
- [~] Instructions executable without oral context — `corpus/fixtures/README.md`; no box checked.
- [~] No cross-domain bleed; PROVINCE remains accurate — `.shokunin/lore/PROVINCE.md`, no game-mechanics or rights claims; no box checked.

No promotion requested or self-attested.
