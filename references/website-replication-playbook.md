# Website Reference Replication Playbook

Use this playbook when a user provides a website URL, screenshot, recording, or reference project and asks to recreate or closely match its UI/UX. The aim is high, evidence-based fidelity with a functional implementation—not a superficial “inspired by” page.

## 1. Establish the target and boundaries

Record:
- Reference URL(s) and exact pages in scope.
- Target routes/pages and primary user journeys.
- Desktop, tablet, and mobile viewports to inspect.
- Interactions that matter (navigation, search, filters, menus, dialogs, tabs, forms, scrolling, hover/focus).
- Existing app constraints, framework, backend/API boundaries, and components that must be preserved.
- Whether the user owns or is authorized to reuse supplied brand assets.

If the scope is broad, inspect the main landing page and one representative page per distinct template first, then create a route inventory. Ask a question only when a missing detail materially blocks implementation; otherwise state assumptions.

## 2. Inspect the reference systematically

Use a browser or available browsing/automation tool when possible. Do not claim to have visited a URL if the environment cannot access it.

For each in-scope page, inspect:
1. Initial viewport and the full page by scrolling.
2. Header, navigation, footer, overlays, sticky/fixed elements, and page grid.
3. Typography: likely font family, weights, sizes, line heights, line lengths, and text hierarchy.
4. Geometry: max-widths, columns, gutters, section spacing, alignment, card dimensions, border radii, borders, and shadows.
5. Color roles: page background, surfaces, text, muted text, borders, primary action, accent, and status colors.
6. Media: image aspect ratios, crop, focal point, video/poster treatment, icon style, and empty space around assets.
7. Interaction behavior: menus, hover/focus/active states, tabs, accordions, carousels, dialogs, form validation, loading, and error states.
8. Responsive behavior at representative narrow, medium, and wide widths.
9. Motion: what triggers it, direction, duration, easing, stagger, and whether content remains usable without animation.

Maintain an evidence log with columns: observation, evidence/source, confidence (high/medium/low), implementation decision. Separate observed facts from assumptions.

## 3. Build a reference specification before coding

Summarize:
- Page/route inventory and shared shell.
- Component hierarchy and content sections in their correct order.
- Design tokens for color, typography, spacing, radius, shadows, borders, and breakpoints.
- Asset inventory and permitted source for each asset.
- Interaction inventory with expected behavior and states.
- Responsive differences.
- Unknowns and the fallback decision for each.

Do not guess exact measurements when they cannot be observed. Use estimates consistent with the evidence and validate them visually.

## 4. Inspect the user's project before edits

- Read repository instructions and inspect Git status.
- Identify framework, router, entry points, styling system, reusable components, asset folders, APIs, data models, authentication, and tests.
- Map the target reference components to existing project components.
- Preserve working behavior, API contracts, routes, permissions, and unrelated uncommitted changes.
- Decide whether to adapt existing components or add new ones. Avoid rebuilding the app shell unnecessarily.

## 5. Implement in fidelity passes

### Pass A — Structure
Match route structure, section order, page width, grid, column ratios, content density, and major spacing. Ensure the page silhouette resembles the reference before polishing.

### Pass B — Design system
Define shared tokens and components. Match typography hierarchy, colors, surfaces, borders, radii, shadows, and alignment. Avoid arbitrary one-off values where shared tokens fit.

### Pass C — Assets and content
Use user-provided or authorized assets. Match crop, aspect ratio, focal point, and placement. If an asset is unavailable or restricted, create an original substitute with similar composition and tone; disclose that it is a substitute. Do not invent brand assets and present them as originals.

### Pass D — Behavior
Implement the visible and expected interactions. Use real routing and real project data when available. Provide honest integration states for unavailable backend functionality. No dead buttons, fake successful form submissions, or decorative controls pretending to work.

### Pass E — Responsive behavior
Compare at the same or equivalent widths. Adapt layout intentionally: navigation collapse, stacking order, table overflow/alternate layout, image crop, typography scaling, and touch targets. Do not merely shrink the desktop screenshot.

### Pass F — Motion and micro-interactions
Implement purposeful hover, focus, active, open/close, scroll, and transition behavior. Respect reduced-motion settings and keep essential content accessible.

### Pass G — Visual refinement
Compare screenshots and fix differences in this order:
1. Overall structure and section proportions.
2. Main container width, alignment, and whitespace.
3. Typography, wrapping, and line breaks.
4. Major images and their crop.
5. Colors, surfaces, borders, and shadows.
6. Icons, control sizing, and micro-spacing.
7. Motion and subtle interaction details.

## 6. Visual comparison loop

At each major pass:
1. Capture the reference and local implementation at equivalent viewport sizes.
2. Compare side-by-side if screenshot tooling is available.
3. List the five most visually consequential differences.
4. Fix the top differences instead of randomly adjusting CSS.
5. Re-capture and repeat until the agreed acceptance criteria are met or remaining limits are clear.

Check page height and scroll landmarks as well as the first viewport. Avoid overfitting only the hero area.

## 7. Functional and quality checks

Verify as applicable:
- All target routes load and navigation destinations are correct.
- Menus, tabs, accordions, dialogs, carousels, filters, and forms work.
- Loading, empty, success, validation, and failure states are meaningful.
- Keyboard navigation, focus visibility, labels, contrast, and reduced motion work.
- Narrow, medium, and wide layouts have no accidental overflow or clipped controls.
- Existing project tests, lint, typecheck, and build are run where available.
- No new console errors, broken assets, or accidental changes to business behavior.

## 8. Fidelity scorecard

Score each category from 0 to 5, with a short evidence note. Use “not inspected” rather than guessing.

| Category | What to compare |
|---|---|
| Structure | Section order, hierarchy, page silhouette |
| Geometry | Widths, grids, alignment, spacing, proportions |
| Typography | Font character, scale, weight, wrapping |
| Color and surfaces | Backgrounds, contrast, borders, shadows |
| Assets | Image choice, crop, aspect ratio, icon family |
| Interaction | Menus, controls, feedback, forms, navigation |
| Responsive | Layout changes across viewports |
| Motion | Trigger, timing, easing, reduced-motion behavior |
| Accessibility | Keyboard, focus, semantics, contrast |
| Reliability | Routes, errors, existing behavior, tests |

Use the scorecard to guide the next iteration, not to claim objective pixel-perfect accuracy. A high score requires actual comparison evidence.

## 9. Legal, privacy, and access boundaries

- Work only with pages and content accessible to the user and within the user's authorization.
- Do not bypass login, paywalls, anti-bot systems, access restrictions, or technical controls.
- Do not collect private user data or copy credentials, private dashboards, or account-specific information.
- Do not create deceptive impersonation or credential-harvesting experiences.
- Prefer original implementation code. Reuse logos, fonts, photos, videos, and other third-party assets only when the user provides them or their terms permit the intended use.
- When uncertain, recreate the general visual language with original assets and clearly state the limitation.

## 10. Final report for the user

Report:
- Pages and viewports actually inspected.
- Main design patterns and interactions reproduced.
- Exact files/routes changed.
- Visual comparison results and the remaining largest differences.
- Tests and checks actually run.
- Missing assets, inaccessible routes, assumptions, and unimplemented backend dependencies.

Never promise the user will be satisfied or claim a perfect clone without evidence. Aim for a faithful, polished result and close the loop with comparison and verification.
