# lore — round 14 (rejected depth experiment)

Declared before dispatch in `.shokunin/lore/LOG.md`. Baseline report commit `319d3101a7d2396a2170da1fd677be6a00dba0ef` had no supplied wording for the `courier-log` and `archive-ledger` source IDs in the separate r10 fixture. The proposed move was to add newly authored excerpts and a manual claim map without changing JSON or checker behavior.

## Work performed and disposition
- Drafted two explicitly invented/not-recovered excerpts mapping Mira's seal, tick-1 departure, tick-2 arrival, harbor registry and tower bell to existing rows. Non-author reviewer and verifier found no new story fact or meaningful uncertainty; this was retrospective editorial restatement, not substantive lore depth or independent evidence. The two drafts were moved out of active `corpus/fixtures/r10-registry-witness/` to `corpus/live/rejected-r14/` at experiment commit `87ad0095c9db10aa651ee40051ea29cf0ae5e209`; active fixture and checker remain round-13 behavior. Reports `reports/r14-*.md` and append-only LOG closure landed at that commit. All lanes settled without reported failure.

## Landed changes
- `.shokunin/lore/LOG.md` declaration/clarification/rejection, archived drafts `corpus/live/rejected-r14/`, and scoped scout/executor/non-author reviewer/verifier/adjudicator reports at `87ad0095c9db10aa651ee40051ea29cf0ae5e209`. This report lands last. No active capability, no scorecard change, no push or merge.

## Before → after / verdict
Non-author verifier replayed all 28 fixture CLIs against baseline `319d310`: stdout/stderr/exit matched byte-for-byte; 139 fixture JSON hashes and checker matched baseline bytes. Manual clause audit found authored wording correspondence but circular support. Sella's existing “first bell” phrase does not establish numeric tick 1. See `reports/r14-independent-verifier.md`, `reports/r14-reviewer.md`, `reports/r14-axis-adjudicator.md`.

- **Depth unchanged:** new drafts only restated old JSON; archived, not admitted.
- **Coverage unchanged:** no new checker class or assertion.
- **Calibration unchanged:** drafts were clearly labeled newly authored; no independent source truth was established.

**Reject:** no axis improved. The archive is audit evidence, not an active source excerpt or promoted lore-depth claim.

## SHONEN
- [ ] No checkmark earned by this experiment. Existing round-13 state persists; no promotion requested or self-attested.
