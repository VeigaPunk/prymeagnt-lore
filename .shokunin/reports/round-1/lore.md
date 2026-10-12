# lore — round 1 (depth axis-move)

Claim declared before work: “A sourced example bible and a seeded contradiction corpus can be checked by one executable schema-and-consistency checker: the clean bible exits 0, while the contradiction corpus exits 1 and reports every seeded violation.”

## Work performed
- Created a cited fictional example bible and three intentional conflicts: `.shokunin/lore/corpus/fixtures/{consistent,contradictions}/{sources,entities,relations,timeline}.json` at work commit `d094160bbaa4675d966532e15629d0d6ec728750`.
- Implemented schema/citation, dangling-reference, double-booking and timeline-dependency checks: `.shokunin/lore/corpus/fixtures/check_bible.py` at the same commit; no canon is rewritten.
- Recorded decision rules and separately addressed attribution, rights and AI-training permission: `.shokunin/lore/corpus/knowledge/{2026-10-12-lore-decision-table,reference-ledger}.md` at the same commit.
- Independent verifier `lore-r1-independent-verifier` ran both commands after the source edits and confirmed the expected outputs, table boundaries, and no blocker; its read-only reply is corroborated by `.shokunin/lore/corpus/live/runs/20261012T155644Z/{consistent,contradictions}.txt`.

## Landed changes
- `.shokunin/lore/LOG.md` round-1 entry records the claim, results, per-axis verdicts and next move; carried by work commit `d094160bbaa4675d966532e15629d0d6ec728750`.
- `.shokunin/lore/SCORECARD.md` records measurements without inventing quality scores; carried by the same work commit. This report lands after it.

## Before → after measurements
- Baseline mint `de12cb9c1c20d0a3d6c8aebccd282f5dd847cd7a`: `git ls-tree -r --name-only de12cb9 -- .shokunin/lore/corpus/fixtures` returns empty. At work commit `d094160bbaa4675d966532e15629d0d6ec728750`, `python3 .shokunin/lore/corpus/fixtures/check_bible.py .shokunin/lore/corpus/fixtures/consistent` exits **0**, `CLEAN ... 0 violations`; replace `consistent` with `contradictions` and it exits **1**, listing **3** violations: missing-map relation endpoint, arrival's later dependency at tick 3 versus tick 2, and Mira at harbor and tower at tick 2. Both outputs and exit codes are preserved in `corpus/live/runs/20261012T155644Z/`.
- **depth: improved** — executable validation and decision table where the baseline had no checker. **coverage: improved** — four cited record tables and all three seeded conflict classes are tested, but aliases, free-text contradictions and source reliability are not. **calibration: unchanged** — the limits are stated and independently reviewed, but no before-calibration measurement supports an improvement claim. Admission: improved on at least one owned axis; none harmed. Scores intentionally unassigned pending a quality rubric.

## SHONEN
- [~] Real decision tables/error patterns/checklists with cited sources — `corpus/knowledge/2026-10-12-lore-decision-table.md`; independent verifier `lore-r1-independent-verifier` confirmed sources and caveats; box remains unchecked.
- [~] End-to-end domain task executed and logged — `corpus/live/runs/20261012T155644Z/`; named verifier reproduced both exit codes; box remains unchecked.
- [~] Instructions executable without oral context — `corpus/fixtures/README.md`; verifier ran documented commands; box remains unchecked.
- [~] No cross-domain bleed; PROVINCE remains accurate — `.shokunin/lore/PROVINCE.md` and `corpus/knowledge/reference-ledger.md`; verifier found no obvious bleed; box remains unchecked.

No promotion is requested. Reviewer did not edit this work or check any SHONEN box. No push or merge.
