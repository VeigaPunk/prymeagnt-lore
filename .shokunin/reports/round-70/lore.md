# lore round 70 — event-ID pair gate rejected and rolled back

Work/evidence commit `992d7f623fb321b0bde42176ddc8f3c6a6fa58c0` by lore-shokunin <lore@shokunin.local>. Written afterward. No push or merge.

## Work performed
- `.shokunin/lore/LOG.md` declares the event-ID-only calibration candidate and sequential scopes; `reports/r70-executor.md` describes the temporary guard and seven matched fixtures. Non-author `reports/r70-reviewer.md`, `reports/r70-independent-verifier.md`, and Sol `reports/r70-axis-adjudicator.md` separately assess candidate behavior and materiality. Reports and rollback closure landed at `992d7f623fb321b0bde42176ddc8f3c6a6fa58c0`.
- Parent rolled back candidate checker lines, added README subsection and seven new untracked fixture directories after Sol REJECT. No active checker or corpus edit remains.

## Landed changes and verdict
- Work/evidence at `992d7f623fb321b0bde42176ddc8f3c6a6fa58c0` contains LOG and reports only. **Depth unchanged; coverage unchanged in the final unchanged corpus; calibration unprovable-but-better locally for tested candidate, material net gain unproved. REJECT.** The early distinct-pointer warning might still guide repair. No promotion, source-text truth, canon, rights, or mechanics finding.

## Before → after measurements
- Verifier temporarily compared pinned `5ccbffaf4b593dcfa34bf92a8ac351c83a105ab3` checker with the candidate: **130/130** old fixture `(exit, raw stdout, raw stderr)` tuples equal; all seven new controls probed, three missing/blank-ID cases dropped only the pair finding. R62 retained its warning. This measures candidate behavior, not editor repair benefit. After rollback at `992d7f623fb321b0bde42176ddc8f3c6a6fa58c0`, `git diff --name-only 5ccbffaf4b593dcfa34bf92a8ac351c83a105ab3 992d7f623fb321b0bde42176ddc8f3c6a6fa58c0 -- .shokunin/lore/corpus` is empty: no delivered checker, README or fixture delta. Reproduce baseline with `python3 .shokunin/lore/corpus/fixtures/check_bible.py .shokunin/lore/corpus/fixtures/r62-malformed-side` (exit 1, four findings including pair). Exact candidate stdout and limitations are in `reports/r70-independent-verifier.md`; candidate fixtures were deliberately not landed.

## SHONEN
- [~] Decision table/error patterns: matched candidate probes and non-author review, no promotion review.
- [~] End-to-end task: verifier replayed temporary candidate; rejected/rolled back, no promotion review.
- [~] Executable instructions: existing checker invocation and candidate replay in verifier report; no promotion review.
- [~] Province boundary: input-ledger diagnostics only; no source/canon/rights/mechanics inference or promotion review.
