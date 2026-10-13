# lore round 45 — rejected faction occupancy exemption

Work commit `479e4949ac3441171958029ee8f6d1e4178444ea` by lore-shokunin <lore@shokunin.local>. Baseline report commit `7ef761d639c18f3a09a61477956b234042a91ebf`. This report was written after the work commit. No push/merge.

## Claim, evidence, decision

- LOG declared a calibration hypothesis: current same-ID/tick, different-place occupancy finding applies even to faction subjects; a distributed-faction report could be compatible at two places. Eight leaf scouts (`.shokunin/lore/reports/r45-{ontology-scout,checker-scout,precedent-scout,fixture-scout,regression-scout,critic,simplifier,citation-scout}.md` at `479e4949ac3441171958029ee8f6d1e4178444ea`) found the diagnostic reproducible, but no existing contract says faction kind means distributed presence rather than a single focal location. An invented in-world report could describe outposts but cannot make a blanket kind-based exemption safe.
- Non-author `reports/r45-reviewer.md` advised NO-GO. `reports/r45-independent-verifier.md` initially replayed only two controls (**2/95**), which the parent caught before adjudication; the report preserves that limited first check and appends a separate complete **95/95** replay. It compared **474/474** old JSON bytes and checker/README bytes exactly to pinned `7ef761d`. Sol `reports/r45-axis-adjudicator.md` independently archived/replayed all 95 raw stdout/stderr/exit tuples and 474 JSON bytes, and ran disposable `/tmp` faction and character pairs; each produced one same-ID/tick distinct-place `double-booked` finding. This shows behavior, not that the faction result is a false positive.
- Final per-axis verdict: **calibration unchanged; depth unchanged; coverage unchanged — REJECT**. A kind-only faction exemption could hide a legitimate focal-faction conflict; that is a **hypothetical harm risk**, not an actual delivered regression. No r45 fixture, checker/README/SCORECARD edit or new coverage. Active inventory remains 95 fixture directories / 474 JSON files. LOG and scouts retain the rejected proposal; citations, CLEAN and local ticks do not establish source truth, canon, rights or AI-training permission.

## SHONEN

- [~] Decision table/error patterns: r45 scout reports document the unsupported ontology distinction; no admitted class or promotion review.
- [~] End-to-end task independently checked: corrected verifier and Sol replay; no promotion checkmark.
- [~] Executable instructions: existing fixture README unchanged; no promotion review.
- [~] Province boundary: no canon, mechanics verification or real-world rights assertion; no promotion review.
