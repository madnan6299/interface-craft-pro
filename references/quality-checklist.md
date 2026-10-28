# Interface Quality Checklist

## Before implementation
- [ ] Confirm primary user, task, and success outcome.
- [ ] Inspect stack, components, design tokens, and repository instructions.
- [ ] Check Git branch/working tree and preserve unrelated changes.
- [ ] Rank P0/P1 problems before cosmetic polish.

## UX and hierarchy
- [ ] Page purpose and primary action are obvious.
- [ ] Content is grouped by user intent.
- [ ] Typography, spacing, color, borders, and elevation are consistent.
- [ ] Realistic content lengths and data density have been checked.
- [ ] No fake metrics, fake testimonials, or unsupported claims.

## Design-system consistency
- [ ] Global navigation, contextual navigation, and content are visually distinct where needed.
- [ ] Colors, spacing, radii, typography, icons, control heights, and elevation follow reusable tokens.
- [ ] Active navigation and status are not conveyed by color alone.
- [ ] Banners, promotions, and decorative elements do not compete with the primary task.
- [ ] Panels/cards are used for meaningful grouping rather than wrapping every element.

## Interaction and states
- [ ] Every visible control performs its stated behavior.
- [ ] Relevant loading, empty, no-results, error, success, disabled, and permission states are covered.
- [ ] Errors explain how to recover and preserve useful input.
- [ ] Duplicate submission and destructive actions are handled appropriately.
- [ ] Existing business rules, API contracts, permissions, and routes remain intact.

## Responsive and accessible
- [ ] Layout works at narrow, medium, and wide viewports.
- [ ] No unintended overflow or clipped content.
- [ ] Semantic landmarks, headings, labels, and accessible control names are present.
- [ ] Keyboard navigation and visible focus work.
- [ ] Touch targets are practical on mobile.
- [ ] Reduced-motion preferences are respected.
- [ ] Color is not the only way meaning is conveyed.
- [ ] Forms associate actionable errors with fields.

## Motion and performance
- [ ] Every animation has a clear purpose and trigger.
- [ ] Transform/opacity are preferred where appropriate.
- [ ] Essential actions/content are not blocked by decorative motion.
- [ ] Timelines, observers, and listeners are cleaned up.
- [ ] Dependencies are justified and motion remains usable on lower-powered devices.

## Engineering and verification
- [ ] Available lint, typecheck, tests, and build were run or blockers reported.
- [ ] Browser console/network errors were reviewed when tools allow.
- [ ] Git diff was checked for unrelated edits, secrets, and accidental files.
- [ ] Final report separates verified results from assumptions and untested areas.
