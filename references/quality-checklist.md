# Interface Quality Checklist

## Before implementation
- [ ] Confirm the primary user, task, and success outcome.
- [ ] Inspect stack, components, design tokens, and repository instructions.
- [ ] Check Git branch and working tree; preserve unrelated changes.
- [ ] Identify P0/P1 problems before cosmetic polish.

## UX and visual hierarchy
- [ ] Primary action is clear and appropriately placed.
- [ ] Content is grouped by user intent.
- [ ] Typography, spacing, color, borders, and elevation are consistent.
- [ ] Text and controls have adequate contrast.
- [ ] Loading, empty, error, success, disabled, and permission states are covered where relevant.
- [ ] Form errors are actionable and recoverable input is preserved.

## Responsive and accessible
- [ ] Layout works at narrow, medium, and wide viewports.
- [ ] No unintended horizontal overflow or clipped content.
- [ ] Semantic landmarks, headings, labels, and accessible control names are present.
- [ ] Keyboard navigation and visible focus work.
- [ ] Touch targets are practical on mobile.
- [ ] Reduced-motion preferences are respected.
- [ ] Color is not the only way meaning is conveyed.

## Motion and performance
- [ ] Every animation has a purpose and clear trigger.
- [ ] Prefer transform/opacity when appropriate.
- [ ] No essential action is blocked by decorative motion.
- [ ] Timelines, observers, and listeners are cleaned up.
- [ ] Motion remains graceful on lower-powered devices.

## Engineering and verification
- [ ] Existing business rules, API contracts, permissions, and routes are preserved.
- [ ] Visible controls do what their labels promise.
- [ ] Lint, typecheck, tests, and build were run when available.
- [ ] Browser console and network errors were reviewed.
- [ ] Git diff was checked for unrelated edits, secrets, and accidental files.
- [ ] Final report distinguishes verified results from assumptions and untested areas.
