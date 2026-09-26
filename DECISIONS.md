# Decisions

A dated log of every curator decision: approvals, rejections, tier changes, and changes to the rules. Newest entries go at the bottom. Entries are never edited after the fact; a reversal is a new entry that references the old one.

| ID | Date | Decision | Type | Ref |
|---|---|---|---|---|
| D-0001 | 2026-09-26 | Establish the archive as a public repository at `IEISI-ORG/digital-leadership-archive` | Rule | CR-0001 |
| D-0002 | 2026-09-26 | License content under CC BY-NC-SA 4.0 | Rule | CR-0001 |
| D-0003 | 2026-09-26 | Every work, author, lens, dimension and tier requires curator approval. Approving an author does not approve their works; the curator reads and assesses each work | Rule | CR-0001 |
| D-0004 | 2026-09-26 | **Approve work:** Valentine (2016), *Enterprise technology governance: New information and technology core competencies for boards of directors*, QUT Professional Doctorate thesis. Curator read and approved | Approval | CR-0002 |
| D-0005 | 2026-09-26 | Approve eight taxonomy dimensions by name: Leadership level; Industry; Organisation type; Jurisdiction; Competency domain; Technology domain; Evidence type; Leadership function. Definitions and scopes pending | Approval | CR-0004 |
| D-0006 | 2026-09-26 | Systems frameworks (CSH, VSM, SOSM) are applied as lenses in synthesis, not as tags on individual works | Rule | CR-0001 |
| D-0007 | 2026-09-26 | Lenses, including the Valentine competency framework, are first-class objects with a recorded standing | Rule | CR-0001 |
| D-0008 | 2026-09-26 | Standing tiers: Empirical, Practitioner, Myth. The list is open; `unclassified` is the default until evidence is sufficient | Rule | CR-0001 |
| D-0009 | 2026-09-26 | Named tests: "lack of evidence is not evidence of lack"; "popularity is not validity" | Rule | CR-0001 |
| D-0010 | 2026-09-26 | Adoption is recorded separately from usefulness evidence and never counts toward standing | Rule | CR-0001 |
| D-0011 | 2026-09-26 | Case studies are screened (EPISTEMOLOGY.md §4) before they count as usefulness evidence | Rule | CR-0001 |
| D-0012 | 2026-09-26 | Discourse lenses (rhetorical analysis, ontological analysis of language in use) are part of the lens set | Rule | CR-0001 |
| D-0013 | 2026-09-26 | Approve repository structure and two-phase change process (plan, then implementation) | Rule | CR-0001 |
| D-0014 | 2026-09-26 | Record curator interest: the curator is the link between the archive and Digital Directors / Dr Valentine's work | Disclosure | CR-0001 |
| D-0015 | 2026-09-26 | AI assistant in use: Claude (Anthropic) via Claude Code, model Claude Opus 5.5, under the conditions in AI_DISCLOSURE.md | Rule | CR-0001 |
| D-0016 | 2026-09-26 | Approval signal: applying the Paperpile label `DLA-approved` is the curator's approval of a work; the Paperpile commit time is the approval timestamp | Rule | CR-0010 |
| D-0017 | 2026-09-26 | A key removed from the Paperpile export is a withdrawal, logged as a new entry; the work's record is marked withdrawn, not deleted | Rule | CR-0010 |
| D-0018 | 2026-09-26 | Changed fields in the export are metadata corrections recorded at intake; removed fields are flagged to the curator | Rule | CR-0010 |
| D-0019 | 2026-09-26 | Paperpile is the source of truth for fields it can express; other facts are documented overrides with a verifying source | Rule | CR-0010 |
| D-0020 | 2026-09-26 | Abstract export is off; summaries are written from the work itself | Rule | CR-0010 |
| D-0021 | 2026-09-26 | `paperpile-sync` is an untrusted inbox, never merged into `main`; intake compares against the last processed commit | Rule | CR-0010 |
| D-0022 | 2026-09-26 | New or changed export settings are tested against a private target before pointing at the public repository | Rule | CR-0010 |
| D-0023 | 2026-09-26 | Reset the history of `paperpile-sync` to one commit (`d74da36`) to remove earlier exports containing an abstract. Run by the curator; original commit timeline kept in the commit message | Action | CR-0010 |
