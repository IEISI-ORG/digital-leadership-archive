# Templates

Copy the matching template when creating a new object. Front matter fields are the structured data the archive relies on: keep field names unchanged.

| Template | Used for |
|---|---|
| [source.md](source.md) | `sources/<work-id>/index.md` |
| [summary.md](summary.md) | `sources/<work-id>/summary.md` |
| [author.md](author.md) | `authors/<author-id>/profile.md` |
| [author-set.md](author-set.md) | `author-sets/<set-id>/index.md` |
| [dimension.md](dimension.md) | `taxonomy/dimensions/<dim>.md` |
| [tier.md](tier.md) | `taxonomy/tiers/<tier>.md` |
| [lens.md](lens.md) | `lenses/<kind>/<lens-id>/index.md` |
| [case-screening.md](case-screening.md) | Screening a case study (EPISTEMOLOGY.md §4) |
| [change-plan.md](change-plan.md) | `changes/CR-NNNN-<slug>/plan.md` |
| [change-implementation.md](change-implementation.md) | `changes/CR-NNNN-<slug>/implementation.md` |

## Common fields

- `provenance`: `source` | `generated` | `curator` (EPISTEMOLOGY.md §1)
- `review_status`: `draft` | `reviewed`. Only the curator sets `reviewed`.
- `approved_on`, `decision`: date and `D-NNNN` entry in DECISIONS.md.

## Link relations

`cites`, `extends`, `validates`, `critiques`, `refutes`, `origin`, `applies`. Definitions are in the [design spec](../docs/specs/2026-09-26-archive-design.md#3-links-between-works-and-lenses).
