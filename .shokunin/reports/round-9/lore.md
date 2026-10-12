# lore — round 9 (calibration axis-move)

Declared before dispatch in `.shokunin/lore/LOG.md`. Baseline report commit `9e1de5721c0ed6a1f2b8a5749dca07b6959be1f6` reported duplicate timeline IDs, but dependency tick lookup used the last event row with that ID. A tick-3 consumer of `same` (duplicate ticks 1 and 5) thus had different inversion findings depending only on which duplicate appeared last.

## Work performed
- Guarded dependency tick comparison by the count of **schema-valid** event rows. Zero keeps unknown, more than one gets indexed `ambiguous dependency event` with no tick choice, exactly one retains strict-earlier comparison; original duplicate ID, repeat, and self diagnostics remain. Work commit `a2b124d44bcebe51df512dac12d95d088d132883`.
- Added raw fictional order-swapped fixtures `corpus/fixtures/r9-dup-{low-high,high-low}/`, unique control, documentation/decision table, all 19 CLI run outputs `corpus/live/runs/20261012T172227Z/`, and wave reports `reports/r9-*.md`, in the same work commit. All wave members settled with no reported failure.

## Landed changes
- `.shokunin/lore/LOG.md` pre-declaration, clarification, closure; `.shokunin/lore/SCORECARD.md`; checker/fixtures/docs/runs and scout, executor, reviewer, non-author verifier, axis-adjudicator reports at `a2b124d44bcebe51df512dac12d95d088d132883`. This report lands last and cites the work hash. No push or merge.

## Before → after measurement and axis verdicts
Run `python3 .shokunin/lore/corpus/fixtures/check_bible.py .shokunin/lore/corpus/fixtures/<case>`. At baseline `9e1de57`, `r9-dup-low-high` exited 1 with duplicate-ID plus tick inversion; `r9-dup-high-low` exited 1 with duplicate-ID only. At work commit `a2b124d`, both exit 1 with identical duplicate-ID and `timeline[2].depends_on[0]: ambiguous dependency event 'same'`, no invented chronology. `r9-unique-control` exits 0 clean. Saved 19-case outputs `corpus/live/runs/20261012T172227Z/`. Independent non-author verifier replayed all 19, compared all 16 old cases byte-identical to baseline stdout/stderr/exit, verified checker and 94 fixture JSON hashes unchanged before/after, and checked the pair differs only in duplicate target row order. Reviewer probed malformed rows and repeated ambiguous references.

- **Depth unchanged:** no added canon fact or source-text support.
- **Coverage unchanged:** duplicate IDs already produced a finding; this prevents an unwarranted tick inference, not a new rule class.
- **Calibration improved:** ordering of duplicate event rows no longer changes the dependency conclusion. Admit: one improved and none harmed. Only schema-valid event rows count; no source-truth, causal, or game-mechanics claim.

## SHONEN
- [~] Real decision tables/error patterns/checklists with cited sources — `corpus/knowledge/2026-10-12-lore-decision-table.md`, `reports/r9-reviewer.md`; no box checked.
- [~] End-to-end domain task executed and logged — `corpus/live/runs/20261012T172227Z/`, `reports/r9-independent-verifier.md`; no box checked.
- [~] Instructions executable without oral context — `corpus/fixtures/README.md`; no box checked.
- [~] No cross-domain bleed; PROVINCE remains accurate — `.shokunin/lore/PROVINCE.md`; no box checked.

No promotion requested or self-attested.
