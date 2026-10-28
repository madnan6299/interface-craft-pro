# Easy Usage Guide — Interface Craft Pro

You do not need to learn every file before using this skill. Start with the ready-to-use prompt below, give your AI coding agent access to this repository's `SKILL.md`, and describe your project.

## The 3-step quick start

1. **Make the skill available to your coding agent.** If your agent supports repository-based skills, add/import this repository using that agent's normal skill-install method. Otherwise, open `SKILL.md` and paste its instructions into the agent's project instructions. Keep the `references/`, `templates/`, and `integrations/` folders available so the agent can read relevant guides.
2. **Open your project in the agent.** Use the agent in the project workspace (for example, Cursor, Claude Code, Codex, or another coding agent that can inspect files). Tool support varies; do not assume the skill is automatically installed just because the repository is public.
3. **Copy one of the prompts below.** Use the existing-project prompt to improve a current app, or the new-project prompt to build a new interface.

## Ready-to-use prompt: improve an already-developed project

Copy the complete prompt below into your coding agent while your existing project is open:

```text
Use Interface Craft Pro as your UI/UX engineering playbook. Read SKILL.md and only the relevant guides in references/, integrations/, templates/, and tests/ before making changes.

PROJECT CONTEXT
- Project/app: [describe your app]
- Screen, route, or feature to improve: [describe it]
- Main users and their goal: [who uses it and what they need to do]
- Main problems I notice: [optional]
- Constraints: [framework, deadline, browser support, design preferences, etc.]
- Change scope: Improve UI/UX while preserving existing business logic, APIs, database schema, authentication, permissions, routes, and working features unless I explicitly request otherwise.

WORK RULES
1. First inspect the repository instructions, current Git status, app structure, design system, components, routes, APIs, and tests. Do not overwrite or discard unrelated changes.
2. Audit the target flow and rank issues: P0 = broken/risky, P1 = major usability/accessibility, P2 = consistency, P3 = optional polish.
3. Before editing, give me a concise diagnosis, proposed design direction, files likely to change, risks, and acceptance criteria. If the task is clear, proceed without asking unnecessary questions.
4. Reuse the project's stack, tokens, and components. Do not rewrite the whole app or add dependencies unless there is a clear reason.
5. Implement real behavior, not just a pretty mockup. Every visible button, link, filter, menu, and form must work or be clearly marked as intentionally unavailable. Include relevant loading, empty, success, error, disabled, validation, and permission states.
6. Make the experience responsive and keyboard accessible. Use semantic HTML, visible focus, readable contrast, labels, actionable errors, and respect prefers-reduced-motion.
7. Use external design resources only if they are available and appropriate. If unavailable, follow Interface Craft Pro's bundled references and fallback-strategies.md. Do not pretend to have used a tool or library that is not available.
8. Implement the highest-impact improvements first. Preserve existing data contracts and user workflows.
9. Run the checks available in this project (lint, typecheck, tests, build, and browser checks when possible). Review the final diff. Never claim checks passed unless you actually ran them.
10. Finish with: summary of improvements, exact files changed, tests/checks and their real results, known limitations, and any follow-up recommendations.

Start by inspecting the project and auditing the specified screen. Do not make destructive changes.
```

## Ready-to-use prompt: build a new project/interface

```text
Use Interface Craft Pro to design and implement a polished, production-minded interface for this new project.

PROJECT
- Product idea: [what you are building]
- Target users: [who will use it]
- Primary user task: [the main thing users need to accomplish]
- Required pages/screens: [list them]
- Required functionality and data: [features, API, database, integrations]
- Preferred stack: [framework/language; if undecided, inspect available environment and recommend a simple fit]
- Visual direction: [brand, light/dark, references, density, tone]
- Constraints: [mobile support, accessibility, performance, browser support, etc.]

INSTRUCTIONS
1. Read SKILL.md and relevant bundled references before implementation.
2. Clarify the information architecture and primary user journey. Make reasonable assumptions explicit rather than blocking on minor unknowns.
3. Inspect the existing workspace before scaffolding; reuse what is already present.
4. Define consistent design tokens and reusable components before duplicating styles across pages.
5. Build functional routes, controls, forms, validation, and relevant loading/empty/error/success states. Do not create dead buttons or fake data presented as real.
6. Design mobile-first and verify narrow, medium, and wide layouts. Use semantic HTML, keyboard support, visible focus, readable contrast, and reduced-motion support.
7. Choose dependencies based on project needs; external Interface Craft Pro references are optional, not mandatory.
8. Implement in small coherent steps and keep the app runnable.
9. Run available lint/typecheck/tests/build checks and review the diff. Report any checks that could not be run.
10. Finish with the implemented pages/features, exact files changed, verification results, and remaining limitations.

Begin with a short implementation plan, then build the first complete, usable end-to-end slice. Do not stop at a static design concept.
```

## Short prompt: polish one screen

```text
Apply Interface Craft Pro to audit and improve [route/screen]. Inspect the existing code first, identify the 3 highest-impact UX issues, then fix them while preserving business logic and API contracts. Ensure responsive layout, accessibility, real interaction states, and purposeful/reduced motion. Run available checks and report exact files changed and verified results. Use bundled guides if external tools are unavailable.
```

## How to get a better result

- **Name the exact screen or workflow.** “Improve my app” is less useful than “Improve the inventory list, filters, empty state, and mobile table behavior.”
- **Explain the real user.** Mention whether this is for customers, accountants, warehouse staff, admins, or another audience.
- **Give constraints.** State the framework, existing design system, APIs that must not change, and what must remain compatible.
- **Ask for a workflow, not only appearance.** Include validation, permissions, errors, loading, success, and empty states.
- **Work in slices.** Improve one flow, verify it, then move to the next rather than redesigning the entire codebase at once.
- **Provide screenshots or references when available.** Explain what to take from them (layout, density, color, interaction) rather than asking for a blind copy.
- **Check evidence.** A visual improvement is not proven until the relevant interactions and available tests have been checked.

## Which files should I read?

| If your task is… | Start with… |
| --- | --- |
| Any UI task | `SKILL.md`, `references/quality-checklist.md` |
| Visual polish or design system | `references/design-foundations.md`, `references/visual-hierarchy.md` |
| Responsive screen | `references/layout-and-responsive.md` |
| Forms and validation | `references/forms-and-validation.md`, `references/accessibility.md` |
| Dashboard or admin panel | `references/dashboard-patterns.md` |
| Landing page | `references/landing-page-patterns.md` |
| Animation | `references/motion-engineering.md`, `references/gsap-recipes.md` |
| Performance | `references/performance.md` |
| External tool/library unavailable | `integrations/fallback-strategies.md` |
| Plan, audit, or final review | `templates/` |

## Important

Interface Craft Pro is a guidance repository, not a guarantee that every coding agent will auto-install it. Follow your agent's supported skill/import mechanism or provide `SKILL.md` as project instructions. Keep the repository files accessible for detailed guidance. The agent must inspect and test your actual project; reading the skill alone does not modify your app.
