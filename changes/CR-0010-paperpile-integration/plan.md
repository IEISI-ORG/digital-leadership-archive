---
cr: CR-0010
title: Paperpile integration as the approval and bibliographic source
status: approved
approved_by: curator
approved_on: 2026-09-26
provenance: generated
---

# CR-0010 Plan: Paperpile integration

## Scope

Make the curator's Paperpile label `DLA-approved` the approval signal and the source of bibliographic data, and document how its automatic BibTeX export is processed. The sync itself is already running (set up and tested on 2026-09-26); this CR records the rules and updates the governing documents.

## Rules to adopt (each becomes a DECISIONS.md entry)

1. **Approval signal.** Applying the Paperpile label `DLA-approved` to a work is the curator's approval of it. The Paperpile commit time on `paperpile-sync` is the approval timestamp.
2. **Withdrawal.** A work whose key disappears from the `.bib` is treated as withdrawn: logged as a new DECISIONS.md entry, never by editing the old one. Its archive record is marked withdrawn, not deleted.
3. **Metadata correction.** Changed fields on an existing key are a correction: recorded in the next intake record, no decision entry. **Removed fields are flagged to the curator** (a DOI was lost once during testing).
4. **Source of truth.** Paperpile owns every field it can express. When it cannot express a fact (e.g. "Professional Doctorate" as thesis level), the archive record adds a **documented override** with a verifying source.
5. **No abstracts.** Abstract export stays off. A work's summary in the archive is written from the work itself, not from its abstract.
6. **Inbox is untrusted input.** `paperpile-sync` is never merged into `main`. Intake compares the `.bib` at the last processed commit with the current one, so a burst of edits counts as one change.
7. **Test export changes privately first.** A new or changed export setting is tested against a private or disposable target before it points at the public repository, because git publishes every version, not only the latest.

## Steps

1. Add `bibliography/README.md` on `main` explaining the inbox branch and rules 1–7.
2. Add a processing record `bibliography/last-processed.txt` holding the `paperpile-sync` commit last processed (starts at `d74da36`).
3. Update `README.md` ("How content gets in"), `AI_DISCLOSURE.md` (condition 3: bibliographic details come from the curator's Paperpile export where available), and the design spec (§7 Workflow).
4. Add rules 1–7 to `DECISIONS.md` as D-0016 to D-0022, and record the history reset of `paperpile-sync` on 2026-09-26 (D-0023).
5. Add `bibtex_key` and `overrides` fields to `templates/source.md`.
6. Update `TODO.md`: CR-0010 done; add CR-0011 (optional: automated check that flags new, removed and changed keys).

## Files affected

New: `bibliography/README.md`, `bibliography/last-processed.txt`, this CR's `implementation.md`.
Changed: `README.md`, `AI_DISCLOSURE.md`, `DECISIONS.md`, `TODO.md`, `docs/specs/2026-09-26-archive-design.md`, `templates/source.md`.

## Out of scope

- Automating intake (GitHub Action or script): proposed as CR-0011, not built now.
- Syncing other labels such as `DLA-reading`.
