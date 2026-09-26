---
cr: CR-0010
status: done
completed_on: 2026-09-26
provenance: generated
---

# CR-0010 Implementation: Paperpile integration

## What was done

- Added `bibliography/README.md` (rules 1–7 and the intake procedure) and `bibliography/last-processed.txt` (set to `d74da36`).
- Updated `README.md` (how content gets in; directory table), `AI_DISCLOSURE.md` (condition 3) and the design spec (§7).
- Logged rules as D-0016 to D-0022 and the branch history reset as D-0023.
- Added `bibtex_key`, `paperpile_commit`, `overrides` and `withdrawn` fields to `templates/source.md`.
- Updated `TODO.md`: CR-0010 done, CR-0002 approved, CR-0011 added.

## Verification

Tested on 2026-09-26 before and during this CR:

- Paperpile pushes to `paperpile-sync` within seconds of each saved edit (commits `4cb99c0` … `3333021`).
- Abstract export switched off: the export at `3333021` has no abstract field.
- After the history reset to `d74da36`, Paperpile pushed `281ee1d` and `6faf3f5` on top of it without error. Abstract lines in branch history: 0.
- All relative Markdown links on `main` resolve (scripted check).

## Deviations from the plan

None.

## Follow-up

- CR-0002 processes the export up to `6faf3f5` and advances `last-processed.txt`.
- The test edit at `6faf3f5` added `address` to the Valentine entry: a metadata correction under rule 3, recorded in CR-0002.
