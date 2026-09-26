# TODO

The formal work list. Each item is a change request (CR) with its own folder in [`changes/`](changes/). A CR moves through: `open` → `planned` (plan written) → `approved` (curator approved the plan) → `done` (implementation recorded).

Priority: **P0** must be done now · **P1** should be done in the current pass · **P2** can wait.

| CR | Title | Priority | Status | Blocked on |
|---|---|---|---|---|
| CR-0001 | Repository skeleton, governing documents, first commit | P0 | done | — |
| CR-0002 | Intake of Valentine (2016): source record, links, draft summary | P0 | done | Curator review of summary |
| CR-0003 | Author profile and author set for Dr Elizabeth Valentine | P0 | open | Curator approval of the author |
| CR-0004 | Define and scope the eight approved dimensions | P1 | open | — |
| CR-0005 | Tier entries for Empirical, Practitioner, Myth in `taxonomy/tiers/` | P1 | open | — |
| CR-0006 | Lens entries: Valentine ETG, VSM, CSH, SOSM, rhetorical analysis, ontological analysis; propose canonical sources as candidates | P1 | open | Curator approval of each canonical source |
| CR-0007 | Candidate discovery: works that apply VSM to governance analysis | P1 | open | — |
| CR-0008 | Candidate discovery: Dr Valentine's later publications and works citing Valentine (2016) | P2 | open | CR-0002 |
| CR-0009 | Propose critical appraisal checklists (e.g. JBI, CASP) as candidates for the case screening protocol | P2 | open | — |
| CR-0010 | Paperpile integration: approval label, sync inbox, intake rules | P0 | done | — |
| CR-0011 | Automated inbox check: flag new, removed and changed keys and removed fields | P2 | open | — |
| CR-0012 | Paperpile MCP integration: read and write the library through Paperpile's MCP server (replaces browser automation and BibTeX export as transport; rules in `bibliography/README.md` unchanged) | P1 | open | Paperpile release. Roadmap status "Started", no date, checked 2026-09-26: https://paperpile.com/roadmap/ |

## Open questions for the curator

- Confirm the wording of the curator interest disclosure in [README.md](README.md).
- Review the draft summary of Valentine (2016), including its reading notes, and confirm or change its `independence: interested` flag.
- Decide on candidates C-0001 to C-0010 in [registers/candidates.md](registers/candidates.md).
