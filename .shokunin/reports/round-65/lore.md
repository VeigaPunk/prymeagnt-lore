# lore round 65 — forward-source alliance gate rejected

Work/evidence commit `e5f69e7e09f19711371dc4d36886b180374ced41` by lore-shokunin <lore@shokunin.local>; pinned baseline r64 report `de1fc0c940d0125f3c61a5183d031468935fcd61`. This report was written after evidence commit. No push/merge.

## No-go and independent evidence

- The declared calibration hypothesis would require the **forward** faction `allied_with` row's source ID to resolve uniquely before emitting a missing sourced-reciprocal finding. Existing code independently reports its citation status, then asks whether a reverse row has a unique source ID. All eight scouts NO-GO; a nine-way temporary matrix showed current behavior, not candidate output. Non-author reviewer independently found unique-forward/absent-reverse yields the reverse-needed pointer; unknown-forward/absent-reverse yields **both** direct unknown citation and missing reverse pointer; unknown-forward/unique-reverse yields an unknown forward citation and a **reverse-row** missing qualified witness. The existing `r7-ally-reverse-ambiguous` control with a distinct unique forward source has exactly three findings (duplicate reverse source ID, reverse citation ambiguity and forward missing qualified reciprocal). Synthetic duplicated source IDs can affect multiple other citations; they do not isolate a direction or prove treaty content.
- Independent verifier and Sol each archived pinned `de1fc0c`, matched **1,298/1,298** full corpus file paths/raw bytes, **623/623** old fixture JSON and **125/125** raw stdout/stderr/exit tuples. Sol repeated matched directional probes and judged **calibration unchanged/material benefit unproved; depth unchanged; coverage unchanged — REJECT**. The direct citation error and missing reverse edge identify different repairs; suppressing the latter risks hiding a pointer without a demonstrated better decision. No checker candidate, fixture or README change exists, so this is no-change preservation, not candidate regression. Corpus remains 125 fixture dirs / 623 JSON paths. Source ID membership is not source-text support, fictional alliance truth, chronology, canon, rights/license/permission.

## SHONEN

- [~] Decision table/error patterns: forward/reverse source-status matrix and rejected gate recorded; no promotion review.
- [~] End-to-end task independently reviewed/replayed: no-change reviewer/verifier/Sol, no checker gain.
- [~] Executable instructions: active checker and README untouched.
- [~] Province boundary: structural input-edge/citation check only, not treaty truth, canon/rights or game mechanics; no promotion review.
