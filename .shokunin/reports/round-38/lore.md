# lore round 38 — rejected coverage experiment

Experiment/archive commit `e025dc6e1c36e26a182e3fda568ddf0fc1fdd55f` by lore-shokunin <lore@shokunin.local>. Baseline report commit `ceb6ea7c2c609dfc332218ceb14f04994f5c28c6`. This report was written after the experiment commit. No push/merge.

## Work performed and disposition

- Pre-dispatch one-axis claim and eight leaf scouts: `.shokunin/lore/LOG.md` round 38 at `e025dc6e1c36e26a182e3fda568ddf0fc1fdd55f`; reports `.shokunin/lore/reports/r38-{source-scout,precedent-scout,pair-scout,regression-scout,critic,simplifier,scribe,citation-scout}.md`. The precedent scout found r7 reviewer's **temporary ledger `claim_a` source-ambiguity probe**; LOG corrected the overbroad first-coverage premise before fixture implementation.
- Scoped executor copied r35 to unique/ambiguous Bell-7 pairs, only appending an identical `sella-bell7-note` source row in the negative. Named non-author reviewer/verifier confirmed exact outputs and baseline preservation (`reports/r38-{executor,reviewer,independent-verifier}.md`). Final `reports/r38-axis-adjudicator.md` independently replayed and **rejected** the axis claim: opposite `claim_b` side, Bell-7 context and durability repeat r7's already tested source-status branch; they are not a material coverage gain.
- Moved the pair from active fixtures to `corpus/live/rejected-r38/` for audit. The active fixture README gives runnable archive commands. LOG closure records the rejection. `SCORECARD.md` remains round 37. The archived example is not counted as active coverage; no checker/prior fixture JSON change.

## Before → after evidence and verdict

- At baseline `ceb6ea7`, no r38 fixture (`git ls-tree -r --name-only ceb6ea7 -- .shokunin/lore/corpus/fixtures/r38-` → empty). The temporary pair showed control exit 0/CLEAN, duplicate exit 1 with exactly three findings: `sources[4].id` duplicate, `contradictions[0].claim_b.source_id` ambiguous and collateral `timeline[3].source_id` ambiguous. These remain reproducible at `corpus/live/rejected-r38/` after archival, not active fixture paths. Independent verifier and adjudicator each matched **90/90** old stdout/stderr/exit and **449/449** old JSON bytes at `ceb6ea7`.
- **Coverage unchanged, depth unchanged, calibration unchanged; none harmed. REJECT: no axis improved.** A valid source ID check neither authenticates testimony nor resolves the Bell-7 reports, canon, rights or permission. The repeated checker branch does not merit an axis gain merely because this audit example is committed.

## SHONEN

- [ ] Rejected experiment earns no checkmark or promotion review. `SCORECARD.md` remains at r37. No push/merge.
