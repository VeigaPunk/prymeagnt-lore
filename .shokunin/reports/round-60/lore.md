# lore round 60 — distinguish unavailable entity table from loaded absence

Work commit `308180f24556ad60dec45747040d64c8317634fb` by lore-shokunin <lore@shokunin.local>; pinned baseline r59 report `d76619452cea837eeb95b1196683b29175b0c98a`. This report was written after the work commit. No push/merge.

## Delivered calibration move

- Round declaration, eight independent scouts and scoped candidate are in `.shokunin/lore/LOG.md` and `.shokunin/lore/reports/r60-*.md` at `308180f24556ad60dec45747040d64c8317634fb`. Some scouts recommended NO-GO to **broad** suppression; the implemented move gates only entity-dependent checks when the full `entities.json` file cannot load as a JSON array. A loaded empty or partial array still produces absent-from-loaded-index diagnostics. Source citation, tick/dependency, schema and other independent checks remain. This is not a source/canon/world-absence conclusion.
- Executor's initial unavailable fixture also had independent timeline faults. Parent corrected it to match `r60-empty` and `r60-partial` byte-for-byte across the other four tables; the faults remain separately in `r60-unavailable-independent`. The executor's initial four-violation unavailable result is historical, not the current matched fixture result. Non-author reviewer verified the matched bytes and **PASS**ed narrow material calibration. Pinned non-author verifier independently observed **98/99** prior raw stdout/stderr/exit tuples identical; only `r59-nested-duplicate` changed **7→1**, retaining its duplicate-member load diagnostic while withholding six dependent dangling findings. All **494** old JSON paths/bytes unchanged.
- Sol independently audited **1,169** old corpus paths (1,167 byte-identical, checker+README changed, 20 new JSON paths), the 99 old raw tuples and same-byte candidate inputs. Current matched unavailable emits file error only (1); loaded empty emits six dangling findings; loaded partial emits three. Unavailable-independent retains load error, negative tick, unknown source and unknown dependency (4). Missing and nonarray probes show same availability policy. Sol: **calibration materially improved; depth unchanged; coverage unchanged — ADMIT**, no material harm observed. Suppressed lines were useful as rough affected-reference hints but not warranted missing-reference conclusions. Loaded arrays with rejected malformed rows remain “available” with lookups over retained valid rows; unavailable sources/timeline remain out of scope. Inventory 103 fixture dirs / 514 JSON paths. No real or fictional absence, source-text truth, chronology, canon, rights, license or permission determined.

## SHONEN

- [~] Decision table/error patterns: matched load-state controls demonstrate input-index versus unavailable status; no promotion review.
- [~] End-to-end task independently reviewed/replayed: r60 reviewer/verifier/Sol; no promotion checkmark.
- [~] Executable instructions: checker and fixture README specify entity-only policy and row-filter limitation; no promotion review.
- [~] Province boundary: structural input validation only, not world/canon, rights, or game-mechanics verification; no promotion review.
