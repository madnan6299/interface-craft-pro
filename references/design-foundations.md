# Design Foundations

Use this file as the self-contained baseline when external UI libraries or design references are unavailable.

## Start with the user job
Describe the screen in one sentence: who is using it, what they need to finish, and what a successful outcome looks like. Organize the interface around that job, not around internal database tables or the list of features the team happens to have.

## Information hierarchy
- Give each page one dominant purpose and one clear primary action.
- Put high-frequency information before rare details; keep secondary actions visually quieter.
- Group related controls by user intent. Separate unrelated tasks with spacing and headings, not decorative boxes alone.
- Prefer meaningful labels and examples over clever but ambiguous copy.
- Keep important context visible during multi-step tasks.

## Visual system
Define semantic tokens before applying ad-hoc styling:
- Surfaces: canvas, raised surface, overlay.
- Text: primary, secondary, muted, inverse.
- Borders: subtle, strong, focus.
- Actions: primary, secondary, danger, quiet.
- Status: success, warning, danger, informational.
- Spacing, type scale, radii, elevation, control height, and motion duration.

Use a restrained palette and a consistent spacing rhythm. Contrast, grouping, and alignment should do more work than shadows and gradients. Use gradients, blur, glow, and glass effects only when they support the product's identity and remain legible.

## Density by context
- Operational dashboards and ERP screens may need high information density; preserve scanability with alignment, typography, column consistency, and compact but usable controls.
- Marketing pages need a clear narrative, credible proof, and a visible next step.
- Forms need understandable labels, grouped fields, inline help, and recoverable validation.
- Mobile screens should prioritize the primary task and avoid shrinking a desktop layout into a narrow column.

## Content and trust
Use realistic content to test layout. Avoid filler repeated across cards, fake metrics presented as facts, dead links, and controls that look functional but do nothing. Label mock data clearly. Do not fabricate customer quotes, trust badges, performance claims, or compliance claims.

## Decision rule
When visual polish conflicts with clarity, accessibility, performance, or the user's established workflow, prioritize the latter. Make the smallest change that solves the real problem.
