# lore round 27 — coverage

Work commit `55fe508fec502fef5bf6a1f6f81aa93ba5a9529c` by lore-shokunin <lore@shokunin.local>. Baseline report commit `bb4c6c971faeaed48c7dbdf57ceb90fcfc873a21`. This report is written after the work commit. No push/merge.

## Work performed

- Pre-dispatch single-axis claim and scoped wave plan: `.shokunin/lore/LOG.md` round 27 at `55fe508fec502fef5bf6a1f6f81aa93ba5a9529c`. Eight leaf scout reports `.shokunin/lore/reports/r27-{both-scout,pair-scout,citation-scout,regression-scout,critic,simplifier,scribe,schema-scout}.md` precede the fixture edit.
- Added matched `corpus/fixtures/r27-target-only/` and `r27-both-ambiguous/` bibles: the latter adds exactly one admitted, `courier-log`-referencing duplicate `mira` entity with empty claims to the target-only duplicate-`seal` case. The relation and four other JSON tables are byte-identical (`reports/r27-executor.md`, `55fe508fec502fef5bf6a1f6f81aa93ba5a9529c`). Checker unchanged.
- Non-author `reports/r27-reviewer.md` inspected pair and collateral timeline findings; `reports/r27-independent-verifier.md` replayed all prior fixtures; `reports/r27-axis-adjudicator.md` independently ran pair and judged axes. All committed at `55fe508fec502fef5bf6a1f6f81aa93ba5a9529c`.

## Landed changes

- `LOG.md`, `SCORECARD.md`, fixture README, ten new JSON files and eleven scoped reports landed in `55fe508fec502fef5bf6a1f6f81aa93ba5a9529c`; no checker edit. The LOG closure cites independent replay and the two collateral timeline findings. This report cites the completed work commit, not its own hash.

## Before → after measurements

- Before baseline `bb4c6c9`: no r27 fixture paths (`git ls-tree -r --name-only bb4c6c9 -- .shokunin/lore/corpus/fixtures/r27-target-only .shokunin/lore/corpus/fixtures/r27-both-ambiguous` → empty). After at `55fe508fec502fef5bf6a1f6f81aa93ba5a9529c`: `python3 .shokunin/lore/corpus/fixtures/check_bible.py .shokunin/lore/corpus/fixtures/r27-target-only` exits 1 with duplicate `seal` and `relations[0].to` ambiguity (2 total); same command on `r27-both-ambiguous` exits 1 with duplicate `seal`, duplicate `mira`, **both** `relations[0].from` and `.to` ambiguity, and **two collateral** `timeline[i].entity_id` actor ambiguity findings (6 total). `reports/r27-independent-verifier.md` confirms 76/76 prior stdout/stderr/exit exact and 379/379 prior JSON paths unchanged. The adjudicator independently confirmed the pair.
- Per-axis verdict: **coverage improved**, **depth unchanged**, **calibration unchanged**, none harmed (`reports/r27-axis-adjudicator.md`). This is one simultaneous-endpoint fixture test, not a canon or relationship-truth finding.

## SHONEN

- [~] Decision tables/checklists: fixture README round 27 and `reports/r27-scribe.md`; no promotion review.
- [~] End-to-end task logged and non-author replayed: `LOG.md` round 27, `reports/r27-independent-verifier.md`; no SHONEN checkmark review.
- [~] Executable instructions: fixture README pair commands; no promotion review.
- [~] Province boundary: `PROVINCE.md` and `reports/r27-citation-scout.md`; no source-text/canon or game-mechanics claim; no promotion review.
