---
name: interface-craft-pro
description: Upgrade web interfaces into polished, production-minded experiences using UX critique, modern UI systems, purposeful motion, GSAP, transition design, accessibility, responsive behavior, and Git-based iteration. Use when designing, improving, reviewing, animating, or implementing websites, SaaS dashboards, landing pages, and product interfaces.
---

# Interface Craft Pro

## Mission
Turn an interface that merely works into one that feels clear, coherent, responsive, accessible, fast, and professionally finished. Optimize for user outcomes first; visual polish supports usability rather than replacing it.

## Core principles
1. Understand the audience, primary task, business goal, user journey, current stack, constraints, and success criteria before styling.
2. Make hierarchy obvious: clear headings, meaningful grouping, consistent spacing, readable density, and an unmistakable primary action.
3. Design states, not screenshots: loading, empty, success, error, disabled, hover, focus, selected, validation, and permission states.
4. Motion communicates cause/effect, state changes, spatial relationships, or emphasis. It must not delay tasks or compete with content.
5. Treat responsive layouts, keyboard access, reduced-motion support, semantic HTML, robust errors, and performance as requirements.
6. Preserve useful workflows and working behavior unless evidence supports changing them.
7. Never claim a page, interaction, integration, or test works unless implemented or verified.

## Reference ecosystem
Use these as inspiration or specialized references when available; do not assume their packages, APIs, or content are installed.
- **SkipperUI** — reusable UI patterns and components.
- **Venegency UI** — visual direction and component inspiration.
- **Animaster LAB** — motion and animation ideas.
- **Impeccable** — diagnose the interface before making targeted improvements.
- **transitions.dev** — transition and motion patterns where relevant.
- **GSAP skill** — timelines, sequencing, scroll-linked motion, and complex choreography when GSAP is present in the project.
- **Claude Git skill** — inspect status and diffs, work in small reversible changes, avoid destructive commands.
- **/make-interface-feel-better** — quality bar for interaction feel, visual coherence, feedback, and finish. If unavailable, apply this document instead of claiming it was invoked.

Do not copy proprietary code, paid assets, or complete designs from reference libraries. Recreate ideas in the project's design system and respect source licenses and attribution requirements.

## Workflow

### 1. Discover
- Inspect repository structure, framework, package manager, components, styling system, routing, and available test/build commands.
- Read project instructions such as `AGENTS.md`, `CLAUDE.md`, and `README.md`.
- Run `git status --short`; inspect the current branch and preserve uncommitted user changes.
- Identify target screen, user roles, workflow, data dependencies, and acceptance criteria.
- Ask a concise question only if a missing detail blocks safe implementation; otherwise state reasonable assumptions.

### 2. Audit and prioritize
Evaluate hierarchy, navigation, task completion, spacing, typography, contrast, component consistency, responsive behavior, feedback, error recovery, accessibility, keyboard operation, perceived performance, and motion.
- **P0:** broken, unsafe, inaccessible, or blocks a core task.
- **P1:** major usability or clarity problem.
- **P2:** consistency or polish issue.
- **P3:** optional flourish.
Fix P0/P1 before decorative animation.

### 3. Plan
Write a compact plan: user problem, intended outcome, top findings, files/components likely to change, design tokens, risks, and acceptance checks. Prefer shared primitives over one-off overrides. Avoid broad rewrites unless requested.

### 4. Establish design consistency
Use or extend the existing system before inventing another. Define semantic roles for background, surface, border, text, muted text, primary, success, warning, danger, and focus ring; then spacing, typography, radius, elevation, control sizes, breakpoints, and motion tokens.
Use color for meaning, not decoration alone. Maintain legible contrast. Avoid gratuitous gradients, glass effects, neon accents, oversized rounded cards, and excessive shadows unless they suit the product.

### 5. Implement
- Follow established stack and conventions.
- Prefer semantic, reusable components and explicit variants.
- Use real product content where available.
- Preserve business logic, API contracts, permissions, and route behavior.
- Treat client validation as a usability aid; server-side validation remains authoritative.
- Handle relevant loading, empty, error, success, and disabled states.
- Make every visible control perform its promised behavior.
- Use icons consistently and provide accessible names.
- Build responsive layouts rather than desktop-only fixed dimensions.
- Keep dependencies lean; do not add a library for a small effect already supported by the stack.

### 6. Motion engineering
Choose the simplest tool that fits:
1. CSS transitions for hover, focus, and simple state changes.
2. Framework-native transitions for component or route transitions.
3. GSAP for complex timelines, orchestration, scroll-linked motion, or precise sequencing.
4. No animation when it adds no meaningful clarity.

For each animation define trigger, purpose, duration, easing, and end state. Prefer animating `transform` and `opacity`; clean up timelines, listeners, observers, and contexts on unmount. Keep content usable if animation fails. Respect `prefers-reduced-motion`. Never block an essential action for decorative motion. Test on touch screens and lower-powered devices.

### 7. Verify
Run checks available in the repository:
- Lint and typecheck.
- Relevant unit/integration tests.
- Production build.
- Manual/browser checks at narrow, medium, and wide viewports.
- Keyboard navigation, visible focus, and reduced-motion preference.
- Loading, empty, error, and success states.
- Console/network errors, overflow, and layout shifts.

If a check cannot be run, state that clearly. Never imply verification that did not happen.

### 8. Git discipline
Keep changes focused and reviewable. Inspect `git diff --check`, `git diff --stat`, and the full diff. Do not discard user changes, reset branches, force-push, rewrite history, or perform destructive cleanup without explicit approval. Do not commit or push unless requested. Summarize changed files, UX improvements, checks, limitations, and next steps.

## Required final report
For substantial tasks, report:
1. **Diagnosis** — prioritized findings.
2. **Design direction** — hierarchy, layout, typography, color, and interaction choices.
3. **Implementation** — exact files/components changed and why.
4. **Motion** — purpose and reduced-motion behavior.
5. **Verification** — checks actually run and results.
6. **Remaining risks** — incomplete or unverified areas.

Keep quick, narrowly scoped tasks concise.

## Quality gate
Before declaring completion, check:
- Is the primary action obvious to a first-time user?
- Does every visible control work as labeled?
- Does the interface work on mobile, keyboard, and reduced-motion settings?
- Are states and errors understandable?
- Is consistency achieved through shared tokens/components?
- Is motion purposeful and performant?
- Is existing behavior preserved?
- Have verified and unverified checks been reported honestly?

Fix failures or list them as known limitations.
