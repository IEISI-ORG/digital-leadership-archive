# Bibliography inbox

The curator's Paperpile library is the source of approvals and of bibliographic data for this archive (CR-0010).

- Paperpile label: **`DLA-approved`**
- Automatic BibTeX export to branch [`paperpile-sync`](https://github.com/IEISI-ORG/digital-leadership-archive/tree/paperpile-sync), file `bibliography/DLA-approved.bib`
- Last `paperpile-sync` commit processed into `main`: [`last-processed.txt`](last-processed.txt)

The `.bib` file is **not** copied to `main`. Each work's archive record in [`sources/`](../sources/) carries its citation fields and its BibTeX key.

## Rules

| # | Rule |
|---|---|
| 1 | **Approval signal.** Applying `DLA-approved` in Paperpile is the curator's approval of a work. The Paperpile commit time is the approval timestamp. |
| 2 | **Withdrawal.** A key that disappears from the `.bib` is a withdrawal: logged as a new entry in [DECISIONS.md](../DECISIONS.md), and the work's record is marked withdrawn, not deleted. |
| 3 | **Metadata correction.** Changed fields on an existing key are corrections, recorded in the next intake record. **Removed fields are flagged to the curator.** |
| 4 | **Source of truth.** Paperpile owns every field it can express. Facts it cannot express are added in the archive record as documented `overrides`, each with a verifying source. |
| 5 | **No abstracts.** Abstract export is off. Summaries are written from the work itself. |
| 6 | **Untrusted inbox.** `paperpile-sync` is never merged into `main`. Intake compares the `.bib` at the last processed commit with the current one, so a burst of edits counts as one change. |
| 7 | **Test export changes privately.** A new or changed export setting is tested against a private or disposable target before it points at this public repository. |

## Intake procedure

1. `git fetch origin` and compare `bibliography/DLA-approved.bib` between the commit in `last-processed.txt` and `origin/paperpile-sync`.
2. Classify each difference: new key (approval), removed key (withdrawal), changed or removed field (correction).
3. Open or extend a change request for each approval or withdrawal; list corrections in its implementation record.
4. After the change is merged, update `last-processed.txt` to the processed commit.
