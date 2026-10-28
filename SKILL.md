---
name: interface-craft-pro
description: A self-contained UI engineering skill for auditing, recreating, implementing, animating, and verifying polished web interfaces. Use when improving existing projects, building new interfaces, or recreating a public website from user-provided URLs, screenshots, or references. External libraries are optional; bundled references and fallbacks are sufficient.
---

# Interface Craft Pro v2.1

## Mission
Deliver interfaces that help people complete real tasks with clarity, confidence, accessibility, consistency, and speed. For website references, reverse-engineer the visible experience systematically and recreate its important visual and interaction patterns in the user's project—not merely a vague approximation or static screenshot. This repository is the primary operating manual. External sites, packages, plugins, and agent commands are optional enhancements, never required dependencies.

## Operating contract
- Inspect the actual project before choosing an implementation.
- Preserve business rules, APIs, permissions, routes, data shape, and useful behavior.
- Make the smallest coherent change that solves the highest-impact user problem.
- Implement working behavior and states, not a static mockup presented as a finished feature.
- Use original implementation code and user-authorized assets; do not copy proprietary source, paid assets, private data, or protected materials without permission.
- Never claim a test, browser check, integration, or build passed unless it was actually run.
- Prioritize correctness, accessibility, user intent, and project conventions over visual novelty.
- A reference is evidence to inspect, not permission to invent details or ignore constraints.

## Start here
1. Inspect repository instructions, framework, routes, design system, package manager, and tests.
2. Check Git status and preserve uncommitted work.
3. Identify the target user, primary task, data dependencies, constraints, and success criteria.
4. If a website reference is supplied, follow `references/website-replication-playbook.md` before implementation.
5. Audit the interface and rank findings P0 (blocks or risks), P1 (major usability), P2 (consistency), P3 (optional polish).
6. Read only relevant guides: foundations and hierarchy; responsive layout and typography; accessibility and forms; interactions and motion; landing-page or dashboard patterns; performance; optional integrations and fallbacks.
7. Make a concise plan, implement, verify, and report limitations honestly.

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

### 4. Reference-driven recreation
When the user gives a website URL, screenshot, recording, or visual reference:
- Treat the task as a structured reverse-engineering exercise. Inspect the reference before coding; do not jump directly from its name to implementation.
- Follow the phases, evidence log, and comparison loop in `references/website-replication-playbook.md`.
- Recreate the design language and meaningful user experience: page structure, spacing, type scale, color roles, surfaces, navigation, responsive behavior, interactions, transitions, and key UI states.
- Use available browser tools to inspect multiple routes and viewport sizes. If browser access is unavailable, say so and work from supplied screenshots, assets, or observations; never pretend to have browsed.
- Identify assets only from accessible and authorized sources. Prefer assets supplied by the user or assets clearly permitted for reuse. When unavailable, create suitable original replacements; do not hotlink protected assets or claim exact asset parity.
- Implement all relevant routes and controls in scope. For links or forms that depend on unavailable backend services, build a clear integration boundary and honest state rather than faking a successful transaction.
- Compare the local implementation with the reference in repeated passes: structure → proportions → typography/color → assets → interactions → responsive behavior → details.
- Aim for high visual and behavioral fidelity, but never claim pixel-perfect equivalence without evidence. Explain inaccessible pages, missing assets, uncertain details, and scope limits.
- Do not bypass login, paywalls, anti-bot controls, access restrictions, or collect private data. Do not reproduce deceptive pages intended to impersonate a service or capture credentials.

### 5. Motion
Use CSS for simple transitions, framework-native tools for standard component transitions, and GSAP only for complex timelines or scroll choreography when installed and justified. Define trigger, purpose, timing, easing, end state, interruption behavior, reduced-motion alternative, and cleanup. Never hide essential content behind animation.

### 6. Verify
Run available lint, typecheck, tests, and production build. Inspect narrow, medium, and wide widths; keyboard/focus; reduced motion; meaningful states; console/network errors; overflow; and core flows where tooling permits. For reference-driven work, also compare screenshots at equivalent viewport sizes and record the remaining visible differences. Record what actually ran and what did not.

### 7. Git discipline
Inspect status, diff, diff summary, and whitespace errors. Preserve unrelated edits. Do not reset, force-push, rewrite history, delete user work, or commit/push unless explicitly requested.

## Optional reference ecosystem
SkipperUI, Venegency UI, Animaster LAB, Impeccable, transitions.dev, GSAP resources, Claude Git guidance, and /make-interface-feel-better are optional references. Do not assume a resource is online, installed, maintained, licensed for copying, or callable. Check integrations/resource-registry.md; if unavailable, use integrations/fallback-strategies.md. Never block work because an external reference is offline.

## Required final report
For substantial work, report: diagnosis and priority; design decisions and user benefit; exact files changed; accessibility and motion behavior; verification actually performed; known limitations, assumptions, and next steps. For website recreation, additionally report inspected routes/viewports, implemented interactions, visual comparison results, and any unavailable reference details/assets.

## Quality gate
Use references/quality-checklist.md and tests/skill-quality-checklist.md. Fix P0/P1 failures before declaring completion; explicitly list anything unverified.
