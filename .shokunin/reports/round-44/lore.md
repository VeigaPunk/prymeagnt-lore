# lore round 44 — rejected actor-kind rule

Work commit `ff6a5f3f16d20bcf8e5b3c296f1c57818a7a1509` by lore-shokunin <lore@shokunin.local>. Baseline report commit `83d62fcde1badb26adfc6c0a99fd17dcd91c782a`. This report was written after the work commit. No push/merge.

## Claim, evidence and decision

- LOG declared a coverage hypothesis: `timeline.entity_id` accepts a unique place even though the README describes character occupancy. It explicitly required proof of a character-only contract before a kind guard. Eight disjoint Luna scouts (`.shokunin/lore/reports/r44-{ontology-scout,checker-scout,precedent-scout,fixture-scout,regression-scout,critic,simplifier,citation-scout}.md` at `ff6a5f3f16d20bcf8e5b3c296f1c57818a7a1509`) found the field generic and no such ontology contract. R11 validates `place_id` kind, while r12/r21 address actor ID and occupancy, not an actor-kind requirement.
- Fixture scout and Sol adjudicator each made disposable `/tmp` clones of `consistent/` with first event `entity_id` changed `mira` → `harbor`; both control and altered checker calls exited 0/CLEAN. This observes acceptance **only**. The altered event description still says Mira departed; the checker does not assess prose or decide whether a place-subject event is valid. No committed r44 fixture or checker/README/SCORECARD change. An unconditional `not a character` finding might reject legitimate place/faction/item-subject events; this is a calibration-harm *risk*, not observed harm.
- Named non-author `reports/r44-reviewer.md` recommended no-go. Verifier and Sol adjudicator independently archived baseline `83d62fc`, matched **95/95** raw stdout/stderr/exit tuples, **474/474** prior JSON bytes and checker bytes; no r44 fixture. Sol `reports/r44-axis-adjudicator.md` at `ff6a5f3f16d20bcf8e5b3c296f1c57818a7a1509` gave **coverage unchanged; depth unchanged; calibration unchanged — REJECT**. Replay preservation is not an axis gain. Source citation/ID and CLEAN do not establish truth, character-only ontology, canon, rights or permission.
- LOG retains the rejected candidate, scout and review evidence and final verdict. No axis scorecard change; active inventory stays 95 fixture directories / 474 JSON paths.

## SHONEN

- [~] Decision table/error patterns: r44 scouts explain the generic-entity boundary; no new admitted error class or promotion review.
- [~] End-to-end task independently replayed: r44 verifier and Sol reports; no promotion checkmark.
- [~] Executable instructions: existing README unchanged; no promotion review.
- [~] Province boundary: no game-mechanics verification, real-world rights claim or canon inference; no promotion review.
