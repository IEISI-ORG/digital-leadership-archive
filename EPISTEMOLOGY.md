# Epistemology

This file sets out how the archive decides what counts as evidence, how it classifies the standing of lenses, and how it marks where each statement comes from. The rules apply to the works studied and to the archive's own text.

## 1. Provenance: where each statement comes from

Every statement in the archive is one of three kinds.

| Kind | Meaning | How it is marked |
|---|---|---|
| **Source** | Quoted or paraphrased from an approved work | Page reference to the work |
| **Generated** | Drafted by the AI assistant | `provenance: generated`, with `review_status: draft` or `reviewed` |
| **Curator** | The curator's own judgement | `provenance: curator`, or a passage marked **Curator assessment** |

The conditions on AI-generated content are in [AI_DISCLOSURE.md](AI_DISCLOSURE.md).

### Independence

Evidence produced or funded by the owner, vendor or promoter of a lens is flagged `independence: interested`. It is not excluded, but the reader can see who is vouching for the lens. The same rule applies to the curator: see the curator interest disclosure in the [README](README.md).

## 2. Standing tiers

A **lens** is any framework, model or method used to understand digital leadership. Each lens has a standing that summarises the evidence for it.

| Tier | Meaning | Required evidence |
|---|---|---|
| **Empirical** | Supported by empirical work presented for peer review. The gold standard for academic claims. | Linked approved works that validate the lens |
| **Practitioner** | Established in practice, not empirically validated, and no contradicting empirical work found within a stated search scope | Credible case studies that pass screening (section 4), and a dated search statement (below) |
| **Myth** | Popular, but has failed scrutiny | Linked approved works that refute it, and the kind of failure |

A Myth records one of two kinds of failure:

- `failed-empirical`: the lens was tested and failed. Example: MBTI.
- `method-invalid`: the method behind the lens cannot produce valid evidence, so it cannot count as empirical. Example: the Dunning–Kruger effect, where the statistical model has been criticised as producing the effect by construction.

These examples illustrate the tiers. They are not classifications: a lens enters a tier only when approved works in the archive support it.

### Rules for tiers

1. **The list of tiers is open.** Other tiers may be added as the evidence shows patterns the current ones do not fit. Each tier is defined, scoped and approved like a taxonomy dimension, in [taxonomy/tiers/](taxonomy/tiers/).
2. **`unclassified` is the default.** A lens stays unclassified until the curator decides the evidence is sufficient. The archive does not assign a tier to fill a blank.
3. **No tier without linked evidence.** Every tier assignment links to the approved works it rests on.
4. **Search statements are bounded and dated.** The Practitioner rule is never written as "nothing contradicts it". It is written as: *"As of YYYY-MM-DD, no contradicting empirical work was found in [search scope]."*
5. **Myth requires positive refutation.** A lens enters the Myth tier only on refuting evidence, never on missing support.
6. **Tier changes are curator decisions.** A newly approved contradicting work flags a lens for review; it does not change the tier by itself. Every change is logged in [DECISIONS.md](DECISIONS.md) with the work that prompted it.

### Adoption is not usefulness

Each lens records two separate facts:

| Field | Records | Counts toward standing? |
|---|---|---|
| **Adoption** | Market reach, certifications, use in education or standards | **No**, context only |
| **Usefulness evidence** | Evidence that applying the lens produces the outcome it claims | **Yes**, the only input to a tier |

Commercial success does not test usefulness. A lens with wide adoption and failed usefulness evidence shows the gap that marks a Myth.

### Scope of validity

A lens's standing is recorded against the taxonomy: which values of which dimensions the evidence covers (for example, *Board × multiple industries × Australia*), and where the lens is being used beyond its evidence.

## 3. Named tests

These tests apply to every text in the archive, AI-generated or not, and serve as rhetorical lenses on the works studied.

| Test | Catches |
|---|---|
| **Lack of evidence is not evidence of lack** | Treating the absence of a finding as a finding. "No study shows it fails, so it works." |
| **Popularity is not validity** | Treating adoption, sales or fame as evidence. "Used by most of the Fortune 500." |

New tests are added by curator decision and logged in [DECISIONS.md](DECISIONS.md).

## 4. Case study screening

A case study counts as usefulness evidence only after screening. The question is: **is this a sales pitch, or a real result from a proper test of the framework?**

| # | Test | Question | Sales-pitch signal |
|---|---|---|---|
| 1 | Independence | Who wrote it, and who paid for it? | Written or funded by the vendor or delivering consultant |
| 2 | Selection | How was this case chosen? | Only successes shown |
| 3 | Attribution | Would the result have happened anyway? | No baseline, no comparison, other changes at the same time ignored |
| 4 | Outcome definition | Was success defined before the work began? | Vague outcomes, or goals redefined afterwards |
| 5 | Measurement | How was the outcome measured, and by whom? | Satisfaction or testimonials only |
| 6 | Fidelity | Was this framework actually what was applied? | Framework bundled with other interventions |
| 7 | Duration | Was the result measured long enough afterwards? | Measured right after delivery only |
| 8 | Verifiability | Could a third party check it? | Anonymous organisation, no checkable detail |
| 9 | Rhetoric | Does the text argue, or sell? | Superlatives, calls to action, the named tests failing |

Outcomes:

- **Credible case:** counts as usefulness evidence.
- **Weak case:** recorded with its flaws listed; adds nothing to standing.
- **Sales material:** adds nothing to standing; kept as data for the discourse lenses.

Established appraisal checklists may later be adapted for this protocol. Any such checklist is a source and needs curator approval first.

## 5. Summaries describe; synthesis interprets

- A **work summary** reports what the work says, with page references. It does not apply lenses.
- A **synthesis** applies one or more lenses (systems, domain or discourse) to a group of approved works, and is marked as interpretation.

## 6. Scope of this file

Changes to this file follow the change process and are logged in [DECISIONS.md](DECISIONS.md).
