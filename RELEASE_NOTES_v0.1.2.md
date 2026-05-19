# What's new in v0.1.2

## Features

- **Execution timeline bar** ([#95](https://github.com/zenml-io/kitaru-ui/pull/95)) — Interactive timeline above the checkpoint thread. Colored segments are proportional to duration; hover shows name / type / duration; click a segment to scroll the matching row into view with a brief highlight ring. Wait blocks render as warning-colored segments alongside checkpoints.
- **Delete executions** ([#115](https://github.com/zenml-io/kitaru-ui/pull/115)) — New "Delete" action available from both the execution detail header and table rows. Confirmation requires typing `DELETE`. On success, the cache is invalidated and you're navigated back to the flow overview.
- **Truncated-text tooltips** ([#98](https://github.com/zenml-io/kitaru-ui/pull/98)) — Long memory keys, artifact names, and checkpoint names now show a tooltip on hover *only* when the text is actually clipped — no more guessing what got cut off, no noise when it fits.

## Fixes

- **Timeline bar with cached checkpoints** ([#99](https://github.com/zenml-io/kitaru-ui/pull/99), [#116](https://github.com/zenml-io/kitaru-ui/pull/116)) — Cached (zero-duration) checkpoints now render as the smallest visible pill instead of disappearing, and the bar fills the full width when every checkpoint is cached. Large checkpoint counts now scroll horizontally.

## UI polish ([#96](https://github.com/zenml-io/kitaru-ui/pull/96))

- Checkpoint detail header and tabs share a single `bg-card` container with one border.
- `CheckpointTypeBadge` uses a softer `rounded-sm` shape with a subtle border.
- `ArtifactChip` and `MemoryChip` are larger and easier to click; `MemoryChip` swaps its color dot for a database icon.
- Artifact text (code blocks, JSON viewer, markdown) bumped from `text-2xs` to `text-xs` for readability.

## Internal

- Replaced `@untitledui/icons` with `lucide-react` ([#113](https://github.com/zenml-io/kitaru-ui/pull/113)).
- Extracted shared `DetailList` component ([#93](https://github.com/zenml-io/kitaru-ui/pull/93)).
- Dependency updates ([#97](https://github.com/zenml-io/kitaru-ui/pull/97)).

**Full Changelog:** https://github.com/zenml-io/kitaru-ui/compare/v0.1.1...v0.1.2
