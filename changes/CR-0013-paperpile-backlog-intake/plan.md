---
cr: CR-0013
title: Intake of the 2026-09-30 Paperpile backlog (seven works)
status: planned
approved_by:
approved_on:
provenance: generated
depends_on: CR-0010
---

# CR-0013 Plan: Intake of the 2026-09-30 Paperpile backlog

## Scope

Process the `paperpile-sync` export from `6faf3f5` (last processed) to `2a8a713` (10 commits, 2026-09-30 06:31–09:50 UTC). The comparison found seven new keys, no removed keys and no changes to the existing key `Valentine2016-qx`.

Each new key is an approval under D-0016. The approval timestamp is the commit where the work first carried `DLA-approved`. For the two re-keyed works this is the commit that added the original key (see "Re-keyed before intake").

| Key at `2a8a713` | Work | First approved | Proposed work ID |
|---|---|---|---|
| `Caluwe2019-ny` | Caluwe, L., & De Haes, S. (2019). Board level IT governance: A scoping review to set the research agenda. *Information Systems Management, 36*(3), 262–283. doi:10.1080/10580530.2019.1620505 | `481f4be` 2026-09-30T06:48:43Z | `caluwe-2019-board-itg-scoping-review` |
| `Opdenbusch2025-xy` | Opdenbusch, J. C., Hielscher, J., & Sasse, M. A. (2025). "Where are we on cyber?" A qualitative study on boards' cybersecurity risk decision making. *NDSS Symposium 2025*. doi:10.14722/ndss.2025.240595 | `481f4be` 2026-09-30T06:48:43Z | `opdenbusch-2025-boards-cyber-risk` |
| `Elms2026-cj` | Elms, N., Nowland, J., & Weerasinghe, A. P. (2026). STEM expertise in Australian boardrooms: Trends and impact on firm outcomes. *Journal of Accounting Literature, 48*(5), 302–326. doi:10.1108/jal-07-2025-0373 | `481f4be` 2026-09-30T06:48:43Z | `elms-2026-stem-expertise-boards` |
| `Longo2024-lp` (key will change, see below) | ASIC (2024). *Beware the gap: Governance arrangements in the face of AI innovation* (Report 798) | `dfdc687` 2026-09-30T06:36:45Z | `asic-2024-rep798-ai-governance` |
| `Longo2025-oj` | Longo, J. (2025, 12 March). *The times they are a-changin' – but directors' duties aren't* [Speech, AICD Australian Governance Summit]. ASIC | `fe6ad26` 2026-09-30T06:38:24Z (as `UnknownUnknown-ky`) | `longo-2025-directors-duties-speech` |
| `Australian-Securities-and-Investments-Commission2026-ct` | ASIC (2026, 27 May). *ASIC Chair Joe Longo speaks on Tech Council of Australia panel* [Panel transcript] | `fa69966` 2026-09-30T06:38:33Z (as `UnknownUnknown-ww`) | `asic-2026-tech-council-panel` |
| `Crowe2026-ao` | Crowe, I. (2026, 5 April). Australian boards lack AI tech experts: QUT reveals gap. *Academic Jobs* | `15aa2a2` 2026-09-30T06:31:09Z | `crowe-2026-boards-ai-expertise-news` |

### Re-keyed before intake

`UnknownUnknown-ky` became `Longo2025-oj` at `36eba55`, and `UnknownUnknown-ww` became `Australian-Securities-and-Investments-Commission2026-ct` at `a9293e5`. `main` never processed either original key, so neither change is a withdrawal under D-0017. The implementation record will note both re-keyings.

### Correction needed in Paperpile before implementation

`Longo2024-lp` lists **Joseph Longo** as author. ASIC REP 798 names ASIC as author, both in the PDF metadata (`Author: ASIC`) and on the title page. Longo signed only the foreword (PDF p. 3). Under D-0019, Paperpile holds this field, so the curator corrects it there:

- author: `{Australian Securities and Investments Commission}`
- institution: ASIC
- number: 798
- month: October

Paperpile will then re-key the entry, probably to `Australian-Securities-and-Investments-Commission2024-…`. This is a metadata correction of a key not yet processed, so it needs no decision entry. Implementation starts from the export commit that contains this correction.

## Steps

1. **Re-check the inbox.** Fetch `paperpile-sync` and confirm the REP 798 correction is present. Compare against `6faf3f5` again, and fold in any later changes.
2. **Log approvals.** Add D-0024 to D-0030 to `DECISIONS.md`, one per work. Each entry reads "Approved via `DLA-approved` label", with the first-approval commit and time. Entries do not say the curator has read the work unless the curator confirms that.
3. **Records.** For each work, create `sources/<work-id>/index.md` from its Paperpile entry, following `templates/source.md`:
   - `bibliography_verified: true` only after cross-checking against the publisher or DOI record. Otherwise `false`, with the reason given.
   - `access` checked at intake. Open: Opdenbusch (NDSS), REP 798, both ASIC pages, Crowe. To be checked: Caluwe (Taylor & Francis), Elms (Emerald).
   - Taxonomy tags use the approved dimension names only. Values are provisional until CR-0004.
   - `independence` is proposed for each work as a draft for the curator to confirm.
   - `authors` list author IDs only. No author records are created (CR-0003 precedent: authors need separate approval).
4. **Read and summarise.** For each work whose full text can be reached, read it in full from a local scratch copy (never committed). Then write `summary.md` from the work itself: question, method and evidence, findings, frameworks used, stated limitations, with page or section references. Descriptive only, `review_status: draft`. A paywalled work gets a record but its summary stays pending, marked `access: paywalled` in the record, until the curator provides a copy.
5. **Check.** Apply the named tests to each summary and record the check in its front matter. Record what kind of source each work is:
   - Peer-reviewed empirical work: Caluwe, Opdenbusch, Elms.
   - Regulator review: REP 798.
   - Regulator statements: speech and panel.
   - Secondary news report: Crowe.
   Statistics a work repeats from another source are marked secondary, with that source named.
6. **Candidates.** Add to `registers/candidates.md`, with `nominated_by: ai`, `status: proposed` and `unverified` until checked:
   - The QUT study that Crowe (2026) reports on.
   - The Governance Institute of Australia 2024 Board Diversity Index and the KPMG report, both cited by Longo (2025) for the 7% and 69% figures.
   - Works each summary identifies as foundations of, or direct tests of, its main claim, limited to three per work.
7. **Links.** Record links between the new works where a work states the relation itself. For example, Elms (2026) measures the effect of the board expertise that Longo (2025) calls for. No link is inferred without a page reference.
8. **Close out.**
   - Set `bibliography/last-processed.txt` to the processed commit.
   - Add the seven works to `sources/README.md`.
   - Update `TODO.md`.
   - Write this CR's `implementation.md`, listing re-keyings, corrections and flagged items.
   - Make one commit per work, then one commit for the close-out.

## Items flagged for the curator

- **Elms (2026)** carries issue date 14 December 2026, after today's date (2026-09-30). This is probably an early-view article dated to a future issue. It will be checked against the Emerald record and noted, not changed.
- **ASIC 2026 panel transcript.** It contains many "[inaudible]" gaps, and one Longo passage breaks off mid-sentence in the published text. The summary will quote only passages that are complete.
- **Crowe (2026)** is a news report of a study, not the study itself. The study is proposed as a candidate (step 6).

## Curator review needed after implementation

- Each summary (draft → reviewed).
- Taxonomy tags and `independence` flags.
- Proposed candidates.

## Files affected

New:
- `sources/<work-id>/index.md` and `summary.md` for seven works (summaries only where full text is reachable).
- This CR's `implementation.md`.

Changed:
- `DECISIONS.md`
- `sources/README.md`
- `registers/candidates.md`
- `bibliography/last-processed.txt`
- `TODO.md`

## Out of scope

- Author profiles for any of these authors (would each need approval, as in CR-0003).
- Tier or standing for any lens (CR-0005, CR-0006).
- Automated inbox checking (CR-0011).
