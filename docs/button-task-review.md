# Button Task Review

## Findings
1. No automated test committed for the button task.
The Playwright checks were executed via temporary scripts under `/tmp`, so the repo still has no repeatable test asset for this change. This is acceptable given the instruction to avoid new dependencies, but it does limit regression protection. `docs/button-task.md`

2. Global `.btn:hover` applies to all buttons including specialized ones.
This is currently overridden by more specific selectors for primary, filter, and danger states, but any future button variants without explicit hover styles will inherit the generic gray hover. That may not be desired for new variants. `src/index.css`

## Correctness vs requirements
- Primary styling: Add and Save use `btn__primary` and share the same styling. `src/components/Form.jsx` `src/components/Todo.jsx` `src/index.css`
- Destructive styling: Delete uses `btn__danger` with hover. `src/components/Todo.jsx` `src/index.css`
- Filter selected state: `aria-pressed` styling uses a strong contrasting background; selected state is clear. `src/components/FilterButton.jsx` `src/index.css`
- Hover states: defined for all buttons, with specific overrides for primary, filter, and danger. `src/index.css`

## Edge cases
- If a new button variant is introduced without explicit hover styles, it will fall back to the generic `.btn:hover`. This is fine for neutral buttons but could be inconsistent for other variants. `src/index.css`

## Accessibility
- Button focus styles remain intact via the global `:focus-visible` outline, and selected filter state is not solely indicated by underline but by color contrast. `src/index.css`
- Hover-only indicators are not required for keyboard users; focus rings remain. `src/index.css`

## Performance / regressions
- CSS-only changes; no runtime performance impact expected.
- Slight behavior change: filter selected state no longer uses underline but uses filled background. This is aligned with the requirement for a clear selected state. `src/index.css`

## Lint / build status
- Not run in this review.

## Test coverage
- No committed tests. Playwright checks were run via temporary scripts and are not part of the repo. `docs/button-task.md`

## Risks and follow-ups
- Risk: Future button variants may unintentionally inherit generic hover styling.
Follow-up: If new button variants are added later, add explicit hover styles or a neutral base class.
- Follow-up: If repeatable UI tests are desired, add a Playwright/Vitest setup and commit a minimal smoke test when dependency additions are allowed.
