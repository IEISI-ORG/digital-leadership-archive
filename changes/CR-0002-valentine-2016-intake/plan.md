---
cr: CR-0002
title: Intake of Valentine (2016)
status: approved
approved_by: curator
approved_on: 2026-09-26
provenance: generated
depends_on: CR-0010
---

# CR-0002 Plan: Intake of Valentine (2016)

## Scope

Create the archive record and a draft summary for the approved work (D-0004):

> Valentine, E. L. H. (2016). *Enterprise technology governance: New information and technology core competencies for boards of directors* [Professional Doctorate thesis, Queensland University of Technology]. https://eprints.qut.edu.au/93089/

## Steps

1. **Record.** Create `sources/valentine-2016-etg-thesis/index.md` from the Paperpile entry `Valentine2016-qx` (commit `d74da36`), with one override: `thesis_type: Professional Doctorate` (source: QUT ePrints record 93089).
2. **Read.** Download the open-access PDF from QUT ePrints to the local scratch area (never committed) and read it in full.
3. **Summarise.** Write `summary.md` from the thesis itself: question, method and evidence, findings (including the competency set), frameworks used, stated limitations. Page references throughout. Descriptive only; no lens interpretation. `review_status: draft`.
4. **Check.** Apply the named tests to the summary; record the check in its front matter.
5. **Tags and links.** Draft taxonomy tags using the approved dimension names only (values provisional until CR-0004 defines them), and record works the thesis builds on as link targets. Link targets not in the archive are listed as possible candidates in `registers/candidates.md` with `nominated_by: ai` and `status: proposed`; none are added to the archive.
6. **Update** `sources/README.md`, `TODO.md`, and log the intake in this CR's `implementation.md`.

## Curator review needed after implementation

- The summary (draft → reviewed).
- The taxonomy tags.
- Any candidates proposed from the thesis's references.

## Files affected

New: `sources/valentine-2016-etg-thesis/index.md`, `sources/valentine-2016-etg-thesis/summary.md`, this CR's `implementation.md`.
Changed: `sources/README.md`, `registers/candidates.md`, `TODO.md`.

## Out of scope

- Author profile and author set for Dr Valentine: CR-0003, needs author approval.
- Lens entry for the Valentine ETG framework: CR-0006.
