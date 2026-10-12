# lore round 23

Lane: lore. Round: 23. Axis-move: depth (lowest owned axis; last change was r15).
Work commit: `08d36f75b0cb3a46fdc3f6a403aeaccf447d9f28` (`git rev-parse HEAD` at report write).
Baseline before this commit: `d6ea676fa43549c85eba6ea9291399db1b970af4`.
Worktree branch is `craft/lore-r1`. The dispatch named `craft/lore-r23`; that branch does not exist in this worktree. Work stayed in `/home/vgpnk/Projects/prymeagnt/lore`.

## Work performed

- Declared the depth move in `.shokunin/lore/LOG.md` before dispatch: one witnessed-absence note class, clause-mapped, with no canon claim.
- Confirmed absence at baseline: `git cat-file -e HEAD:.shokunin/lore/corpus/fixtures/r23-note-class` failed at `d6ea676` (exit 128). Recorded again in `.shokunin/lore/reports/r23-independent-verifier.md`.
- Spawned eight leaf scouts in one turn, each `model='xai/grok-4.5'` and `thinking='low'`: note, clause, schema, critic, simplifier, test, citation, scribe. Reports: `.shokunin/lore/reports/r23-note-scout.md`, `r23-clause-scout.md`, `r23-schema-scout.md`, `r23-critic.md`, `r23-simplifier.md`, `r23-test-scout.md`, `r23-citation-scout.md`, `r23-scribe.md`.
- Wrote fixture `.shokunin/lore/corpus/fixtures/r23-note-class/` from `consistent/` plus speaker Sella, source `sella-absence-note`, and event `strip-absence-note`. Excerpt: Sella looked for Mira’s outbound route strip on the registry hook rack and did not find it. Manual map: `witnessed-absence-clause-map.md`. Checker was not edited and does not read the excerpt.
- Ran `python3 .shokunin/lore/corpus/fixtures/check_bible.py .shokunin/lore/corpus/fixtures/r23-note-class` → exit 0, `CLEAN: schema, citations, relations, timeline; 0 violations`. Adjudicator re-ran the same command (`.shokunin/lore/reports/r23-axis-adjudicator.md`).
- Non-author reviewer `.shokunin/lore/reports/r23-reviewer.md` traced each excerpt clause and compared them to the r15 mark note. Non-author verifier `.shokunin/lore/reports/r23-independent-verifier.md` replayed outputs and hashed baseline JSON.
- Axis adjudicator `.shokunin/lore/reports/r23-axis-adjudicator.md` admitted the round.

## Landed changes

- Fixture, clause map, and excerpt: `.shokunin/lore/corpus/fixtures/r23-note-class/`, tied to the round-23 closure entry in `.shokunin/lore/LOG.md`, carried by `08d36f75b0cb3a46fdc3f6a403aeaccf447d9f28`.
- Decision-table row and fixtures README section for the witnessed-absence class, same LOG entry, same commit.
- SCORECARD depth row updated to round 23, same commit. Coverage and calibration rows unchanged.
- Scout, reviewer, verifier, and adjudicator reports under `.shokunin/lore/reports/r23-*.md`, same commit.
- This report is written after that commit and is not inside it.

## Before → after measurements

- Absence before: `git cat-file -e d6ea676fa43549c85eba6ea9291399db1b970af4:.shokunin/lore/corpus/fixtures/r23-note-class` exits 128. After: the path exists and `python3 .shokunin/lore/corpus/fixtures/check_bible.py .shokunin/lore/corpus/fixtures/r23-note-class` exits 0. Measured at work commit `08d36f75b0cb3a46fdc3f6a403aeaccf447d9f28` by the adjudicator re-run and by the lane replay before commit.
- Prior saved outputs: replay of all 72 files in `.shokunin/lore/corpus/live/runs/20261012T193930Z/` against the current checker matched exit and stdout **72/72**. Counting command: verifier replay recorded in `.shokunin/lore/reports/r23-independent-verifier.md`. Diff count 0.
- Prior fixture JSON: `git ls-tree -r --name-only d6ea676 -- .shokunin/lore/corpus/fixtures` then byte-compare each `*.json` to the worktree. Result: **359/359 same, 0 changed**. The assignment text said 319. That count is the older r22 inventory, not the file count at `d6ea676` (364 fixture files, 359 JSON). The measured count is 359. Forcing 319 would hide 40 paths.

## Verdicts

- depth: **improved**. New inspectable class: a named speaker reports a named thing was not found. Operative clause: “Later at Lantern Harbor, I, Sella, looked for Mira’s outbound route strip on the registry hook rack. I did not find it there.” Not the r15 mark note. Not an r14 restatement.
- coverage: **unchanged**. Checker behavior on the 72 prior saved outputs is exact. The checker still does not read prose.
- calibration: **unchanged**. The note is a report, not proof the strip was absent as fact. It does not deny that Mira carried the seal. It does not mention a mark or the Blue Seal. None harmed.

Admit: yes. Source-text truth remains unverified. No canon claim.

## SHONEN

- [ ] Real decision tables/error patterns/checklists with cited sources. The round-23 row is a local fixture convention, not a cited external source. Untouched.
- [~] End-to-end domain task executed and logged; non-author verifier required. Pointer: `.shokunin/lore/reports/r23-independent-verifier.md` (replay and hash) and `.shokunin/lore/reports/r23-reviewer.md` (clause trace). Not a checkmark: the author did not mark this box, and source-text truth was not verified.
- [ ] Instructions executable without oral context. Untouched.
- [ ] No cross-domain bleed; PROVINCE remains accurate. Untouched. PROVINCE was not edited.

No SHONEN checkmark. No promotion. Push was not attempted: the dispatch branch `craft/lore-r23` is not the branch this worktree is on, and push is operator-owned when the remote path is unclear.
