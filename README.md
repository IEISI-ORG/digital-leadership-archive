# Digital Leadership Archive

A curated, public archive of research on **digital leadership**: how boards, executives and organisations lead with and govern information and technology.

The archive does three things:

1. **Collects approved works** and summarises them, with every work read and approved by the curator before it enters.
2. **Builds a taxonomy of digital leadership** across defined dimensions such as leadership level (board, C-suite), industry and jurisdiction. The dimensions are themselves defined and scoped as part of the taxonomy.
3. **Examines the lenses** used to understand digital leadership (competency frameworks, systems methodologies, commercial models) and records the **standing** of each: what evidence supports it, and where it applies.

The emphasis is on practical frameworks and systems thinking, especially Critical Systems Heuristics (CSH), the Viable System Model (VSM) and the System of Systems Methodologies (SOSM).

> **Status:** skeleton. The structure and rules are in place; content is being added one approved work at a time. See [TODO.md](TODO.md).

## Starting point

The archive starts from the work of **Dr Elizabeth (Lizzie) Valentine**, whose doctoral research produced a validated competency set for board-level technology governance:

> Valentine, E. L. H. (2016). *Enterprise technology governance: New information and technology core competencies for boards of directors* [Professional Doctorate thesis, Queensland University of Technology]. https://eprints.qut.edu.au/93089/ · DOI: [10.13140/RG.2.2.34027.95529](https://doi.org/10.13140/RG.2.2.34027.95529)

Dr Valentine leads Digital Directors ([digitaldirectors.com.au](https://digitaldirectors.com.au)), which provides digital governance advisory and education for boards ([source](https://tilt.io/profiles/digital-directors); see also her [Victoria University of Wellington profile](https://www.wgtn.ac.nz/sim/about/staff/elizabeth-valentine)).

**Curator interest disclosure:** the curator is the link between this archive and Digital Directors / Dr Valentine's work. Works connected to them are subject to the same approval and screening rules as any other work, and this connection is recorded wherever it is relevant.

## How the archive is organised

| Path | Contents |
|---|---|
| [`sources/`](sources/) | One folder per approved work: citation, taxonomy tags, links to other works, summary |
| [`authors/`](authors/) | Profiles of approved authors (public professional information, each claim sourced) |
| [`author-sets/`](author-sets/) | Groups of co-authors and summaries of their research as a body |
| [`taxonomy/dimensions/`](taxonomy/dimensions/) | The dimensions of digital leadership, each defined and scoped |
| [`taxonomy/tiers/`](taxonomy/tiers/) | The standing tiers used to classify lenses |
| [`lenses/`](lenses/) | Frameworks treated as objects of study: `domain/`, `systems/`, `discourse/` |
| [`synthesis/`](synthesis/) | Analyses that apply lenses across groups of works |
| [`registers/`](registers/) | Candidates proposed for approval, and rejected candidates with reasons |
| [`changes/`](changes/) | One folder per change request: plan, then implementation record |
| [`templates/`](templates/) | Front matter templates for every object type |

## How content gets in

Nothing is added unless the curator approves it.

1. A work is **handed in** by the curator (already read and approved), or **proposed** as a candidate in [registers/candidates.md](registers/candidates.md).
2. The curator **reads and assesses** the work, then approves or rejects it. Every decision is logged in [DECISIONS.md](DECISIONS.md).
3. An approved work gets a **summary**, drafted with AI assistance and marked `draft` until the curator reviews it.
4. **Links to other works** (`extends`, `validates`, `applies`, `critiques`, …) are recorded with each work, so chains of evidence build up over time.

Authors, lenses, taxonomy dimensions and standing tiers are approved the same way.

## How claims are judged

[EPISTEMOLOGY.md](EPISTEMOLOGY.md) sets the rules. In short:

- **Standing tiers.** A lens is `Empirical` (peer-reviewed empirical support), `Practitioner` (documented results in practice, and no known empirical contradiction within a stated search scope), or `Myth` (popular, but refuted on evidence or on method). The list of tiers is open, and a lens stays `unclassified` until the evidence is sufficient.
- **Adoption is not usefulness.** Commercial success is recorded, but never counts toward standing.
- **Case studies are screened** for independence, selection, attribution and other flaws before they count as evidence: is this a sales pitch, or a real result from a proper test?
- **Named tests** apply to everything, including this archive's own text: *lack of evidence is not evidence of lack*; *popularity is not validity*.

## Use of AI

This archive is built with AI assistance under stated conditions. See [AI_DISCLOSURE.md](AI_DISCLOSURE.md). In short: the AI drafts and proposes; only the curator approves; every generated statement is marked as generated.

## Change process

Every change to the archive follows two phases, tracked in [TODO.md](TODO.md):

1. **Plan:** `changes/CR-NNNN-<slug>/plan.md` states the scope, steps and files affected. The curator approves it.
2. **Implementation:** `changes/CR-NNNN-<slug>/implementation.md` records what was done and how it was checked.

The design behind this structure is in [docs/specs/2026-09-26-archive-design.md](docs/specs/2026-09-26-archive-design.md).

## Contributing

Suggestions for works, authors or lenses are welcome as [issues](https://github.com/IEISI-ORG/digital-leadership-archive/issues). A suggestion enters the candidate register; it enters the archive only after the curator has read and approved it.

## Licence

Content is licensed under [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0)](LICENSE). Works summarised here remain under their own copyright; this archive links to them and quotes only short passages.

Maintained by [IEISI](https://github.com/IEISI-ORG).
