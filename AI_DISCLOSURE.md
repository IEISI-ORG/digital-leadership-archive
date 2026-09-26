# AI Disclosure

This archive is built with the help of a generative AI system. This file states what the AI does, what it is not allowed to do, and how a reader can tell AI-generated text from human judgement.

If any content in this repository breaks these conditions, treat that content as unreliable and [open an issue](https://github.com/IEISI-ORG/digital-leadership-archive/issues).

## Who is responsible

- **Curator:** Terry Sweetser (IEISI). The curator reads and assesses every work, makes every approval decision, and is accountable for everything published here.
- **AI assistant:** Claude (Anthropic), used through Claude Code. At the time of writing the model is Claude Opus 5.5. Later changes of model are recorded in [DECISIONS.md](DECISIONS.md).

The AI is a tool working under instruction. It is not an author, reviewer or curator of this archive.

## What the AI does

| Task | Output status |
|---|---|
| Drafts summaries of works the curator has approved | `generated`, `draft` until the curator reviews it |
| Drafts research summaries for author sets | `generated`, `draft`; written only from reviewed work summaries |
| Proposes candidate works, authors and lenses | Entered in [registers/candidates.md](registers/candidates.md) as `proposed`; never added to the archive directly |
| Drafts definitions and scopes of taxonomy dimensions and tiers | `generated`, `draft` until approved |
| Drafts case study screenings (see [EPISTEMOLOGY.md](EPISTEMOLOGY.md)) | `generated`, `draft`; the curator confirms each test result |
| Drafts synthesis analyses that apply lenses | `generated`, `draft` until reviewed |
| Maintains structure: files, links, registers, change records | Recorded in the change process |

## Conditions the AI works under

1. **No approvals.** The AI cannot approve, reject or promote any work, author, lens, dimension or tier. Only the curator can, and each decision is logged in [DECISIONS.md](DECISIONS.md).
2. **No additions without approval.** Nothing enters `sources/`, `authors/`, `author-sets/`, `lenses/` or `taxonomy/` unless the curator has approved it. AI suggestions go to the candidate register only.
3. **No citations from memory.** Every bibliographic detail (title, authors, year, venue, DOI, link) is checked against a retrievable record before it is written. A detail that cannot be checked is marked `unverified`.
4. **No claims about people without a source.** Author profiles contain public professional information only, and each claim links to where it was found.
5. **No tier assignments.** The AI may draft the evidence for a standing tier. It never assigns one. A lens stays `unclassified` until the curator decides the evidence is sufficient.
6. **Every generated statement is marked.** Files record `provenance: generated` and `review_status: draft | reviewed` in their front matter. The AI never sets `review_status: reviewed`. The curator does.
7. **Named tests apply to AI output.** Every generated text is checked against the named tests in [EPISTEMOLOGY.md](EPISTEMOLOGY.md), including "lack of evidence is not evidence of lack" and "popularity is not validity".
8. **Summaries describe; they do not interpret.** A work summary reports what the work says, with page references. Interpretation through lenses happens only in `synthesis/`, and is marked as such.
9. **No copyrighted full texts.** The AI does not commit PDFs or full texts. It records links and DOIs, and quotes only short passages with page references.
10. **Changes follow the change process.** Every change has a plan the curator approves before implementation (see `changes/`). AI commits carry a `Co-Authored-By: Claude` trailer, so the git history shows which changes the AI took part in.

## Known limitations

- The AI can misread, compress or distort a source. The curator's review exists to catch this, and draft status stays visible until it has happened.
- The AI cannot read paywalled works unless the curator provides access. Summaries of works it could not read in full say so.
- AI output can sound more confident than the evidence allows. The named tests and the review checklist are there to catch this.

## How to check a statement

1. Look at the file's front matter: `provenance` and `review_status`.
2. Follow the page reference to the original work.
3. Check [DECISIONS.md](DECISIONS.md) for when and by whom the work was approved.
4. Use `git log` on the file to see who changed it and when.
