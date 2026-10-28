---
name: interface-craft-pro
description: A self-contained UI engineering skill for auditing, designing, implementing, animating, and verifying polished accessible web interfaces. Use for landing pages, SaaS dashboards, forms, data-heavy screens, responsive layouts, motion, and UI review. External libraries are optional; bundled references and fallbacks are sufficient.
---

# Interface Craft Pro v2.0

## Mission
Deliver interfaces that help people complete real tasks with clarity, confidence, accessibility, consistency, and speed. This repository is the primary operating manual. External sites, packages, plugins, and agent commands are optional enhancements, never required dependencies.

## Operating contract
- Inspect the actual project before choosing an implementation.
- Preserve business rules, APIs, permissions, routes, data shape, and useful behavior.
- Make the smallest coherent change that solves the highest-impact user problem.
- Implement working behavior and states, not a static mockup presented as a finished feature.
- Use original patterns from this skill; do not copy proprietary source, paid assets, or complete designs.
- Never claim a test, browser check, integration, or build passed unless it was actually run.
- Prioritize correctness, accessibility, user intent, and project conventions over visual novelty.

## Start here
1. Inspect repository instructions, framework, routes, design system, package manager, and tests.
2. Check Git status and preserve uncommitted work.
3. Identify the target user, primary task, data dependencies, constraints, and success criteria.
4. Audit the interface and rank findings P0 (blocks or risks), P1 (major usability), P2 (consistency), P3 (optional polish).
5. Read only relevant guides: foundations and hierarchy; responsive layout and typography; accessibility and forms; interactions and motion; landing-page or dashboard patterns; performance; optional integrations and fallbacks.
6. Make a concise plan, implement, verify, and report limitations honestly.

## Design principles
- Make the main task and next action immediately understandable.
- Use hierarchy, spacing, typography, alignment, and grouping before decoration.
- Establish semantic design tokens and reusable primitives.
- Design for loading, empty, success, error, disabled, selected, validation, and permission states.
- Use purposeful motion with a usable no-motion fallback.
- Optimize for narrow screens, keyboard, assistive technology, slow networks, and error recovery.
- Do not invent product data, fake metrics, or add dead controls.

## Workflow
### 1. Audit
Review information architecture, task flow, hierarchy, consistency, responsiveness, accessibility, error recovery, loading behavior, performance, and existing behavior. Record concrete findings and user impact; avoid vague feedback such as “make it modern.”

### 2. Plan
State the user problem, desired outcome, files likely to change, design direction, risks, and acceptance checks. Ask only if missing information blocks safe progress; otherwise state conservative assumptions.

### 3. Build
- Follow the project's current framework and conventions.
- Prefer shared components, tokens, semantic HTML, and explicit variants.
- Make every visible control perform its stated action.
- Cover relevant loading, empty, success, error, disabled, selected, validation, and permission states.
- Keep server-side validation and authorization authoritative.
- Preserve data contracts and workflows unless change is requested.
- Avoid unnecessary dependencies and placeholder content.

### 4. Motion
Use CSS for simple transitions, framework-native tools for standard component transitions, and GSAP only for complex timelines or scroll choreography when installed and justified. Define trigger, purpose, timing, easing, end state, interruption behavior, reduced-motion alternative, and cleanup. Never hide essential content behind animation.

### 5. Verify
Run available lint, typecheck, tests, and production build. Inspect narrow, medium, and wide widths; keyboard/focus; reduced motion; meaningful states; console/network errors; overflow; and core flows where tooling permits. Record what actually ran and what did not.

### 6. Git discipline
Inspect status, diff, diff summary, and whitespace errors. Preserve unrelated edits. Do not reset, force-push, rewrite history, delete user work, or commit/push unless explicitly requested.

## Optional reference ecosystem
SkipperUI, Venegency UI, Animaster LAB, Impeccable, transitions.dev, GSAP resources, Claude Git guidance, and /make-interface-feel-better are optional references. Do not assume a resource is online, installed, maintained, licensed for copying, or callable. Check integrations/resource-registry.md; if unavailable, use integrations/fallback-strategies.md. Never block work because an external reference is offline.

## Required final report
For substantial work, report: diagnosis and priority; design decisions and user benefit; exact files changed; accessibility and motion behavior; verification actually performed; known limitations, assumptions, and next steps.

## Quality gate
Use references/quality-checklist.md and tests/skill-quality-checklist.md. Fix P0/P1 failures before declaring completion; explicitly list anything unverified.
