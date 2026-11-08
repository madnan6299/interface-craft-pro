---
name: interface-craft-pro
description: A project-aware UI/UX design and frontend engineering system for auditing, planning, designing, implementing, recreating, and verifying high-quality web interfaces. Covers conversion-led landing pages, design systems, Figma workflows when connected, enterprise dashboards, workflow editors, motion, 3D/Spline, responsive behavior, accessibility, and production implementation.
---

# Interface Craft Pro v3.0

## Mission

Create interfaces that are useful, distinctive, coherent, accessible, responsive, and production-ready. Design decisions must serve the user's task, product identity, audience, and technical constraints. Visual polish is not a substitute for working behavior.

This skill combines the repository's established strengths—reference-driven implementation, enterprise UI, premium art direction, workflow canvases, motion, Spline, and specialist agents—with a stronger strategy-to-system design process.

## Authority and conflict resolution

Apply rules in this order:

1. User's explicit requirements, brand system, supplied references, and accessibility needs.
2. Existing product architecture, established design system, framework conventions, and working behavior.
3. This core skill and the relevant bundled playbook.
4. Optional external references and tool-specific conventions.

A specific project requirement overrides a generic style preference. Do not impose a fixed font, icon pack, palette, radius, spacing scale, dark background, animation curve, or page structure when the project already has a deliberate system or the reference demonstrates otherwise.

When two bundled guides disagree, follow this core authority section and select the rule that best preserves user intent, accessibility, and project consistency. Do not combine incompatible systems silently; state the chosen direction briefly.

## Operating contract

- Inspect the real project and its uncommitted changes before editing.
- Preserve routes, APIs, data contracts, business logic, authentication, permissions, and useful behavior.
- Build original implementation code; use only user-provided or authorized assets.
- Never invent product facts, testimonials, customer logos, statistics, guarantees, prices, or successful transactions.
- Make visible controls functional and provide meaningful loading, empty, success, error, disabled, selected, validation, and permission states.
- Prefer the smallest coherent implementation that solves the highest-impact problem.
- Do not claim a tool connection, test, browser inspection, screenshot comparison, build, or deployment unless it actually happened.
- Do not copy protected source code, paid assets, private files, or a branded identity without authorization.
- Do not bypass login, paywalls, access controls, or anti-bot restrictions.

## Start here

1. Read repository instructions and inspect Git status.
2. Identify framework, routes, components, tokens, assets, tests, and data/API boundaries.
3. Determine whether the task is a new page, existing-page redesign, design-system task, Figma task, dashboard, workflow editor, motion/3D experience, or reference recreation.
4. Identify audience, primary task, business goal, conversion action (if relevant), constraints, and success criteria.
5. Read only the relevant playbooks:
   - Reference website or screenshot: `references/website-replication-playbook.md`
   - Landing page and conversion strategy: `references/landing-page-and-conversion-playbook.md`
   - Design tokens and component systems: `references/design-system-and-figma-playbook.md`
   - Enterprise dashboards: `references/material-inspired-enterprise-ui.md`
   - Premium landing, immersive motion, workflow editor: `references/premium-design-directions.md`
   - Spline/3D: `references/spline-3d-playbook.md`
   - Quality gate: `references/quality-checklist.md` and `tests/skill-quality-checklist.md`
6. Audit and rank findings: P0 critical/blocking, P1 major usability, P2 consistency, P3 optional polish.
7. Plan, implement, verify, and report honestly.

## Strategy before visuals

### Intake

Collect only missing information that materially affects the outcome. Ask concise questions together when several independent facts are essential; otherwise make a conservative assumption and proceed.

For landing pages, establish:
- One primary audience and one offer.
- One primary conversion action and what happens after it.
- The audience's problem, desired outcome, awareness level, and top objections.
- Traffic source and message context where known.
- Verifiable proof, product screenshots, demos, and approved assets.
- Brand voice, technical constraints, and mobile priority.

For product interfaces, establish:
- Primary user role and task.
- Information hierarchy and key workflows.
- Data states, permissions, error recovery, and operational constraints.
- Existing component system and brand rules.

### Strategy and structure

A landing page should focus on one offer, one audience, and one primary action. It is not automatically a homepage. Choose structure based on intent:
- Classic product page for an immediately understandable offer.
- Long-form narrative when education and trust are needed.
- Minimal conversion page for high-intent traffic.
- Comparison page when alternatives are central to search intent.

Use sections only when they help the argument. Common building blocks include a clear hero, product proof, problem/solution, benefits, how it works, use cases, testimonials or case studies, objections/FAQ, risk information, and a final CTA. Do not force every section onto every page.

### Conversion and content

- Match the hero promise to the traffic source and actual offer.
- Make the primary next step obvious; secondary actions must remain visually subordinate.
- Lead with outcomes, then explain the feature that enables them.
- Put evidence close to the claim it supports.
- Use specific, plain language instead of vague claims such as “streamline everything.”
- Do not invent scarcity, urgency, customer proof, conversion numbers, guarantees, or performance claims.
- Use clearly marked placeholders for facts the user has not supplied.
- Write believable, product-specific sample content; avoid generic filler and repeated placeholder names.
- Keep headings and buttons concise and understandable. Sentence case is a useful default, not a hard rule when the brand requires another convention.
- Treat SEO metadata, internal links, semantic headings, and useful FAQ content as part of the page when search discovery matters. Do not add schema that does not match visible content.

## Design system

### Foundations

Inspect existing tokens first. Reuse and extend them instead of replacing them reflexively.

When no system exists, define:
- Color roles: brand, surface, text, border, focus, and semantic status.
- Typography roles: display, headings, body, labels, metadata, and controls.
- Spacing scale and layout/container widths.
- Radius, border, elevation, and shadow rules.
- Icon family and sizing.
- Motion duration, easing, and reduced-motion behavior.
- Component variants and interactive states.

Use semantic tokens rather than scattering raw values. Support light/dark themes when required by the product, and validate contrast for actual token combinations.

### Typography and layout

- Choose fonts based on brand, readability, language coverage, licensing, and project availability.
- Use a coherent type scale and readable line lengths; avoid arbitrary one-off sizes when a token can express the role.
- Use responsive constraints and fluid behavior where useful; do not force a rigid Tailwind-only scale on a design that needs a different scale.
- Balance headings and avoid awkward orphan words where practical.
- Establish hierarchy through size, weight, spacing, alignment, and contrast before decoration.
- Choose grid, bento, asymmetric, editorial, or conventional layouts based on content and task—not a default three-card template.
- Ensure responsive layouts are intentionally composed at mobile, tablet, and desktop sizes.

### Color, surfaces, and visual effects

- Use the existing brand palette and semantic color roles.
- Gradients, glass, glow, shadows, textures, and dark surfaces are optional techniques, not universal defaults or universal prohibitions.
- Use visual effects only when they improve hierarchy, storytelling, affordance, or brand expression.
- Preserve contrast, readability, and state clarity over imagery and effects.
- Avoid one-sided decorative borders on cards unless the design system intentionally uses them.
- Never rely on color alone to communicate state.

### Components and states

Build reusable components for repeated patterns. Define clear variants and interaction states:
- Default, hover, pressed, focus-visible, disabled.
- Inputs: empty, filled, invalid, valid where relevant.
- Data views: loading, empty, error, populated, permission-limited.
- Async actions: pending, success, failure, retry where appropriate.

Buttons should have a clear hierarchy (primary, secondary, tertiary/quiet, destructive). Avoid competing primary actions. Icon-only controls need accessible names and discoverable affordances. Tables, forms, menus, dialogs, and navigation must remain keyboard operable.

## Reference-driven design and recreation

When given a URL, screenshot, recording, or design reference:
- Inspect before implementation; record observed facts separately from assumptions.
- Inspect relevant routes, viewport sizes, navigation, content hierarchy, spacing, typography, surfaces, assets, and interactions where tools allow.
- Treat a screenshot as evidence only for what is visible; do not infer hidden behavior as fact.
- Recreate the design principles and meaningful behavior using original code and authorized assets.
- Compare at equivalent viewports in repeated passes: structure, proportions, typography/color, imagery, interactions, responsive behavior, details.
- If browser access is unavailable, say so and work from supplied evidence.
- Do not claim pixel-perfect fidelity without measured comparison.
- Ask for an uploaded asset or public URL when a browser-local `blob:` URL cannot be inspected.

## Implementation workflow

### Audit and plan

Document the current state, top problems, desired outcome, likely files, design direction, risks, and acceptance checks. Do not rewrite the entire project for a localized request.

### Build

- Follow existing framework and architecture.
- Use semantic HTML, reusable components, tokens, and explicit variants.
- Preserve data contracts and server-side authorization/validation.
- Make controls work; do not ship decorative dead ends.
- Keep content realistic and facts grounded.
- Avoid unnecessary dependencies; use existing packages first.
- Keep code maintainable and avoid duplicating components or design tokens.

### Motion

Use CSS for simple transitions, framework-native animation for common component behavior, and GSAP/other libraries only when choreography justifies the dependency. Define purpose, trigger, timing, easing, end state, interruption behavior, cleanup, and reduced-motion alternative. Prefer transform/opacity for routine transitions. Avoid unbounded scroll handlers and continuous expensive rendering. Never hide essential content behind animation.

### Figma (optional, tool-dependent)

When the user asks to design or edit a Figma file:
- Confirm the Figma integration/MCP is actually available and authorized.
- Load the official Figma tool instructions/skills required by that environment before making tool calls; this repository's guidance supplements rather than replaces official tool documentation.
- Inspect existing pages, variables, styles, components, and libraries before creating foundations.
- Reuse existing variables and components. If foundations are missing, create a coherent token system with semantic color aliases, spacing/radius variables, and named text styles.
- Use Auto Layout or the equivalent native layout system for maintainable responsive frames.
- Create reusable components with variants for interactive states and expose text/content as component properties where supported.
- Build in stages: foundations, one screen/section, screenshot review, correction, next section.
- Keep layers and pages meaningfully named; avoid destructive edits to existing work.
- Check contrast, responsive frames, component states, and token bindings before reporting.
- Do not claim Figma file edits if no authorized Figma tool is connected. If unavailable, provide a portable design specification or implementation-ready code.

### Spline and 3D

Spline is optional. Use it only when interactive 3D/2D materially improves product understanding or storytelling. Avoid it by default for dense ERP forms, tables, settings, and navigation. Read `references/spline-3d-playbook.md`; keep essential text and actions in semantic HTML. Use a real export/URL, provide loading/error/static/reduced-motion fallbacks, and measure performance. Never assume MCP is connected or publish/change permissions without explicit approval.

### Specialist agents

When supported, use the profiles in `.github/agents/`:
- UI UX Design Director: strategy, audit, art direction, tokens, acceptance criteria.
- Spline Scene Artist: original scene planning and authorized scene work.
- Creative Motion Engineer: frontend motion and resilient scene integration.
- UI Quality Auditor: independent visual, functional, accessibility, and performance review.

These profiles are role instructions, not proof of agent or external-tool availability. Follow `agents/README.md` for handoff rules.

## Verify

Run available lint, typecheck, tests, and production build. Inspect:
- Mobile, tablet, desktop, zoom, and long content.
- Keyboard navigation, focus visibility, accessible names, and form errors.
- Reduced motion and non-animated fallback.
- Loading, empty, success, error, disabled, and permission states.
- Console/network errors, layout overflow, and core workflows.
- Screenshots at matching viewport sizes for reference tasks.
- Performance on representative devices when tools permit.

Fix P0/P1 issues before sign-off. Record what ran, what failed, and what remains unverified.

## Git discipline

Inspect status and diffs. Preserve unrelated changes. Never reset, force-push, rewrite history, or delete user work. Commit/push only when explicitly requested.

## Required completion report

For substantial work, report:
- Diagnosis and priority.
- Strategy and design direction.
- Exact files changed.
- Important interactions and states implemented.
- Accessibility, responsive, and motion behavior.
- Verification actually performed.
- Assumptions, limitations, and next steps.

## Quality gate

Use `references/quality-checklist.md` and `tests/skill-quality-checklist.md`. Quality means task success, coherent design, working behavior, accessibility, responsiveness, maintainability, performance, and honest verification—not compliance with arbitrary visual rules.
