# lore — round 2 (coverage axis-move)

Claim declared before work in `.shokunin/lore/LOG.md`: a distinct-faction `allied_with` edge needs a separately sourced reciprocal record; a one-way edge must be reported, never silently repaired. Baseline work commit `d094160bbaa4675d966532e15629d0d6ec728750` had no faction symmetry pass.

## Work performed
- Added the scoped checker rule and cited positive/negative fictional faction fixtures: `.shokunin/lore/corpus/fixtures/check_bible.py`, `ally-reciprocal/`, `ally-one-way/` at work commit `fca1f1fc81f493556d929c06e8f7bfb908ce906d`.
- Documented in-world citations, scope and report-only convention: `.shokunin/lore/corpus/fixtures/README.md` and `corpus/knowledge/2026-10-12-lore-decision-table.md`, same work commit. Real-world rights and AI-training permissions are not inferred.
- Eight first-wave leaf reports, executor, non-author reviewer, non-author verifier, and final axis adjudicator reports reside in `.shokunin/lore/reports/r2-*.md` at that commit. All lanes settled without reported failure; `lore-r2-independent-verifier` reran raw inputs and SHA-256 nonmutation check, with caveats recorded in its report.

## Landed changes
- `.shokunin/lore/LOG.md` round-2 declaration and closure and `.shokunin/lore/SCORECARD.md` measurement notes are carried by work commit `fca1f1fc81f493556d929c06e8f7bfb908ce906d`; this report lands afterward and cites that hash. No push or merge.

## Before → after measurements
- Baseline `git show d094160bbaa4675d966532e15629d0d6ec728750:.shokunin/lore/corpus/fixtures/check_bible.py` shows only endpoint/citation checks for relations; no `allied_with` reciprocity. At work commit `fca1f1fc81f493556d929c06e8f7bfb908ce906d`, run `python3 .shokunin/lore/corpus/fixtures/check_bible.py .shokunin/lore/corpus/fixtures/<folder>` for each folder. `consistent` exits **0**, `contradictions` exits **1** with original three errors, `ally-reciprocal` exits **0**, and `ally-one-way` exits **1** with a single `relations[0]` missing-reciprocal violation. Outputs/exit codes are preserved in `.shokunin/lore/corpus/live/runs/20261012T161753Z/`. Named non-author `lore-r2-independent-verifier` reproduced all four and the unknown-source reverse probe, reporting no file mutation.
- **depth: unchanged** — the existing four-table model remains and the new rule is narrow. **coverage: improved** — one new cited relation class distinguishes reciprocal and one-way fixtures. **calibration: unchanged** — scope is explicit, but no before-calibration baseline proves movement. Admit: one improved, none harmed. Reviewer flagged duplicate source IDs as a diagnostic-precision gap; self-edges, nonfaction endpoints, prose, and source semantic truth are outside this rule. See `.shokunin/lore/reports/r2-axis-adjudicator.md` and `r2-reviewer.md`. Scores remain unassigned without a quality rubric.

## SHONEN
- [~] Real decision tables/error patterns/checklists with cited sources — `corpus/knowledge/2026-10-12-lore-decision-table.md`; non-author `lore-r2-reviewer` assessed scope, no box checked.
- [~] End-to-end domain task executed and logged — `corpus/live/runs/20261012T161753Z/`; `lore-r2-independent-verifier` replayed all four, no box checked.
- [~] Instructions executable without oral context — `corpus/fixtures/README.md`; independent verifier used CLI, no box checked.
- [~] No cross-domain bleed; PROVINCE remains accurate — `.shokunin/lore/PROVINCE.md` and reviewer report; no box checked.

No promotion is requested; no SHONEN checkmark is self-attested.
