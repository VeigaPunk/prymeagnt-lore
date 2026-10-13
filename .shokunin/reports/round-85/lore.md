# lore — round 85 (devin host)

**ADMIT — calibration improved (bounded)** (Sol `r85-axis-adjudicator.md`;
mechanical verifier `r85-verifier.md` 5/5; sealed reviewer
`r85-sealed-reviewer.md` operative danger confirmed).

Finding: duplicating a holder entity silently sets `valid=False` (no
diagnostic, unlike the voiced dangling path), then latches
`can_check_chain=False` — a REAL provenance chain break becomes invisible in
checker output. The mask doesn't outrank the break; it switches the check
off. Sealed test: an operator would fix the dup and declare the file clean
under single-pass trust — the break survives.

Probes live outside the admitted corpus (constructed telemetry). Checker
unchanged; repair is a separate declared round. Commits: work `0b45095c`,
report-last this.
