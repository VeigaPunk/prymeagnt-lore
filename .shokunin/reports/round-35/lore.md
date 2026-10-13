# lore round 35 — depth

Work commit `633ba022b45c71a9049664e1d9ac181950820aee` by lore-shokunin <lore@shokunin.local>. Baseline report commit `0b2f4166377622aad45e86cd2204e765b7829e0c`. This report was written after the work commit. No push/merge.

## Work performed

- Pre-dispatch depth claim and eight Luna leaf scopes: `.shokunin/lore/LOG.md` round 35 at `633ba022b45c71a9049664e1d9ac181950820aee`. Scouts `.shokunin/lore/reports/r35-{prior-scout,occasion-scout,ledger-scout,regression-scout,critic,simplifier,scribe,citation-scout}.md` found that a generic shared bell/tick could not support a specific conflicting occasion; the post-scout policy required a single uniquely identified ringing and full-duration Sella absence.
- Added separate `corpus/fixtures/r35-bell7-conflict/`, copied from r33. Newly authored fictional Tarin excerpt says Tarin saw Sella place an unlabeled envelope at Harbor during Bell-7; a separately cited newly authored Sella excerpt claims physical Tower presence throughout that same ringing and no Harbor presence at any point. Both explicitly claim Bell-7 is the sole seventh-watch registry-bell sounding on the seventh day of Embermonth, year 12. The source-claimed date/uniqueness are not externally authenticated. A manual map traces clauses and the two-sided ledger pointers. Tarin's Harbor field is his reported observation **scene**, not a second Sella-actor occupancy record (`reports/r35-executor.md`, `633ba022b45c71a9049664e1d9ac181950820aee`). Checker unchanged.
- **Failure retained:** first non-author `reports/r35-reviewer.md` failed because separately worded “day of this note” could refer to different dates. The executor corrected both excerpts, cited fields and maps before the fresh non-author `reports/r35-remediation-reviewer.md` passed the *conditional report-level* conflict. `reports/r35-independent-verifier.md` replayed baseline; `reports/r35-axis-adjudicator.md` independently replayed and judged axes. All at `633ba022b45c71a9049664e1d9ac181950820aee`.

## Landed changes and measurements

- LOG declaration/policy/failure/remediation/closure, SCORECARD depth row, README, nine new fixture files and twelve scoped reports landed at `633ba022b45c71a9049664e1d9ac181950820aee`; no prior fixture JSON or checker edit. This report cites the completed work commit, not itself.
- Baseline `0b2f416`: no r35 fixture (`git ls-tree -r --name-only 0b2f416 -- .shokunin/lore/corpus/fixtures/r35-bell7-conflict` → empty). At `633ba022b45c71a9049664e1d9ac181950820aee`, `python3 .shokunin/lore/corpus/fixtures/check_bible.py .shokunin/lore/corpus/fixtures/r35-bell7-conflict` exits 0 with exact CLEAN stdout and empty stderr **structurally only**. Both verifier and adjudicator found **86/86** old stdout/stderr/exit exact and **429/429** old JSON bytes unchanged; a preliminary 85/86 verifier replay used inconsistent absolute/relative path spellings on a path-echoing diagnostic and was corrected using identical root-relative argv. Relations table remains byte-identical to r33; Sella source/event and ledger pair are added, while inherited Tarin event and Sella-attributed Tarin claim only receive occasion qualification.
- Per-axis verdict: **depth improved**, **coverage unchanged**, **calibration unchanged**, none harmed (`reports/r35-axis-adjudicator.md`). The two attributed location reports conflict only if their source-claimed single occasion and fixture-local person/place alignments hold. Neither account is chosen; no source truth, canon, Bell-7=tick 3, envelope contents, rights or Blue Seal/carbon/strip inference follows.

## SHONEN

- [~] Decision table/error patterns: `manual-clause-pointer-map.md`, `reports/r35-scribe.md`; no promotion review.
- [~] End-to-end task non-author reviewed/replayed: both reviewer reports and `reports/r35-independent-verifier.md`; no SHONEN checkmark review.
- [~] Executable instructions: fixture README round 35; no promotion review.
- [~] Province boundary: `PROVINCE.md`, `reports/r35-citation-scout.md`; no canon/real-world rights/game mechanics claim; no promotion review.
