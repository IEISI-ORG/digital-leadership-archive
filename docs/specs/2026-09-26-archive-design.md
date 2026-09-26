---
title: Digital Leadership Archive — design
date: 2026-09-26
status: approved
provenance: generated
review_status: draft
---

# Digital Leadership Archive: design

This spec records the design agreed between the curator and the AI assistant on 2026-09-26. The decisions it rests on are logged in [DECISIONS.md](../../DECISIONS.md) (D-0001 to D-0015).

## 1. Purpose

A public, curated archive of research on digital leadership, starting from the work of Dr Elizabeth Valentine (see [README](../../README.md)). It serves three aims:

1. A body of approved works, each read and assessed by the curator, with summaries.
2. A taxonomy of digital leadership across approved dimensions, where the dimensions are themselves defined and scoped.
3. A study of the lenses used to understand digital leadership, including their standing.

Chains of evidence between works are expected to emerge as the body grows. The design records links from the start so those chains become visible, instead of deciding in advance which ones matter.

## 2. Entities

| Entity | Path | Unit | Approved by curator? |
|---|---|---|---|
| Work | `sources/<work-id>/` | One publication | Yes, each one |
| Author | `authors/<author-id>/` | One person | Yes |
| Author set | `author-sets/<set-id>/` | A group of co-authors; a sole author is a set of one | Formed from approved authors |
| Dimension | `taxonomy/dimensions/<dim>.md` | One axis of the taxonomy | Yes, name and definition |
| Tier | `taxonomy/tiers/<tier>.md` | One standing tier | Yes |
| Lens | `lenses/<kind>/<lens-id>/` | One framework, model or method | Yes |
| Synthesis | `synthesis/<topic>.md` | An analysis applying lenses to works | Reviewed |
| Candidate | `registers/candidates.md` | Anything proposed but not approved | — |

Approving an author does not approve their works (D-0003).

### Identifiers

- Work: `<first-author-surname>-<year>-<short-slug>`, e.g. `valentine-2016-etg-thesis`.
- Author: `<surname>-<given-name>`, e.g. `valentine-elizabeth`.
- Author set: member author IDs joined by `+`, sorted alphabetically; for a set of one, the author ID.
- Lens: short lowercase slug, e.g. `vsm`, `csh`, `sosm`, `valentine-etg`.

## 3. Links between works and lenses

Each work records typed links in its front matter:

| Relation | From → to | Meaning |
|---|---|---|
| `cites` | work → work | Cites without substantive use |
| `extends` | work → work | Builds on the other work's findings or framework |
| `validates` | work → work or lens | Provides empirical support |
| `critiques` | work → work or lens | Argues against, without empirical refutation |
| `refutes` | work → work or lens | Provides evidence against |
| `origin` | work → lens | Is where the lens was first set out |
| `applies` | work → lens | Uses the lens, with the taxonomy context it was applied in |

Links may point to works not yet in the archive; these mark candidates that would complete a chain. Example query this supports: *works that `apply` VSM where Leadership function = governance*.

## 4. Taxonomy

Eight dimensions are approved by name (D-0005): Leadership level; Industry; Organisation type; Jurisdiction; Competency domain; Technology domain; Evidence type; Leadership function. Each gets a definition, an in-scope and out-of-scope statement, a reference scheme where one exists (e.g. ANZSIC or GICS for Industry), and a list of values. Leadership level (who leads) and Leadership function (what leadership activity) are deliberately separate.

## 5. Lenses

Lenses are applied in synthesis, not tagged on individual works (D-0006). They are also objects of study with a standing (D-0007).

| Kind | Initial members |
|---|---|
| `domain` | Valentine ETG competency framework |
| `systems` | VSM, CSH, SOSM |
| `discourse` | Rhetorical analysis, ontological analysis of language in use |

A lens entry holds: definition; origin works; standing (tier, evidence, kind of failure where relevant); scope of validity against the taxonomy; adoption (context only); application record (works that `apply` it, and in which contexts); curator assessment.

Commercial frameworks and "myths" (e.g. MBTI, Dunning–Kruger) enter as ordinary lenses when approved.

## 6. Epistemic model

Defined in [EPISTEMOLOGY.md](../../EPISTEMOLOGY.md): provenance kinds, independence flag, open tier list with `unclassified` default, bounded and dated search statements, adoption kept separate from usefulness, named tests, and case study screening.

## 7. Workflow

1. **Intake.** Works arrive handed in by the curator (already approved) or proposed as candidates (by the curator or the AI).
2. **Approval.** The curator reads and decides; the decision is logged.
3. **Summary.** The AI drafts a descriptive summary with page references; the curator reviews it.
4. **Links and tags.** Taxonomy tags and typed links are drafted with the summary and reviewed with it.
5. **Author set summary.** Regenerated only from reviewed work summaries.
6. **Synthesis.** Lens-based analysis across works, marked as interpretation.

Every change follows the two-phase change process: `changes/CR-NNNN-<slug>/plan.md`, curator approval, then `implementation.md`.

## 8. Formats

Markdown with YAML front matter; no build tooling. Templates for each entity are in [`templates/`](../../templates/). PDFs and full texts are not committed (`.gitignore` blocks `*.pdf`).

## 9. Not in scope now

- A static website or search interface.
- Citation-count or practice-adoption measures as inputs to standing.
- Automated validation of front matter. This is worth adding once there are enough files for errors to be likely.
