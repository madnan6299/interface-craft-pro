# Interface Craft Pro

<p align="center">
  <strong>Reference-driven UI engineering for interfaces that look right, feel right, and work right.</strong>
  <br />
  Audit existing products. Recreate reference websites with high visual fidelity. Ship tested, responsive interfaces without breaking core functionality.
</p>

<p align="center">
  <a href="https://github.com/madnan6299/interface-craft-pro"><img alt="GitHub repository" src="https://img.shields.io/badge/GitHub-Repository-181717?style=for-the-badge&logo=github&logoColor=white" /></a>
  <img alt="Self-contained skill" src="https://img.shields.io/badge/Skill-Self--Contained-2563EB?style=for-the-badge&logo=checkmarx&logoColor=white" />
  <img alt="UI UX engineering" src="https://img.shields.io/badge/UI%2FUX-Engineering-0F766E?style=for-the-badge&logo=figma&logoColor=white" />
  <img alt="Reference replication" src="https://img.shields.io/badge/Reference-Driven-6D28D9?style=for-the-badge&logo=googlechrome&logoColor=white" />
</p>

<p align="center">
  <a href="#quick-start">Quick Start</a> ·
  <a href="#copy-paste-prompt">Copy-Paste Prompt</a> ·
  <a href="#reference-website-recreation">Website Recreation</a> ·
  <a href="#capabilities">Capabilities</a> ·
  <a href="#repository-structure">Repository Structure</a>
</p>

---

## Quick Start

**Already have an app? Improve the real project—not just a screenshot or mockup.**

1. Make this repository's skill available to your AI coding agent using its supported skill/import method. If it cannot import repositories as skills, provide `SKILL.md` as project instructions and keep this repository accessible.
2. Open your existing project workspace in an agent that can inspect and edit files, such as Cursor, Codex, Claude Code, or a compatible coding agent.
3. Copy the prompt below, add your project details and any reference URL, then run it.

> Opening or starring this GitHub repository does not automatically install it into your coding agent. Tool capabilities vary by environment.

## Copy-Paste Prompt

Use this single prompt for either **improving an existing UI** or **recreating a website from a reference**. Fill in the relevant fields; leave non-applicable fields blank.

```text
You are a senior UI/UX engineer, design-systems specialist, and reference-driven frontend implementation expert.

MANDATORY SKILL SOURCE — DO THIS FIRST
Use the Interface Craft Pro skill from this repository as your required operating playbook:
https://github.com/madnan6299/interface-craft-pro

1. If this repository is already available in the workspace, open and read its `SKILL.md`.
2. If it is not present locally, retrieve/clone this repository using the tools available in your environment, or open the repository files through an available GitHub/repository connector. Do not assume the skill is installed just because this prompt mentions it.
3. Read `references/website-replication-playbook.md` for reference-website tasks, plus the relevant bundled guides under `references/`, `integrations/`, `templates/`, and `tests/`.
4. If you cannot access the repository or its files, clearly say so before proceeding. Ask me to provide `SKILL.md` and the relevant reference files, or continue only after explicitly noting that you are working without the skill. Do not claim to have used Interface Craft Pro if you could not read it.
5. Follow the skill's inspection, planning, implementation, comparison, accessibility, verification, and final-report workflow. The skill is mandatory for this task, not just a name to mention in the prompt.

OBJECTIVE
Deliver a polished, responsive, accessible, production-minded implementation in my actual project. If I provide a reference website, inspect it carefully and recreate its important visual design, page structure, responsive behavior, and interactions with high fidelity—not a generic page loosely inspired by it.

PROJECT DETAILS
- Project/app: [name and purpose]
- Local project/workspace: [already open in your coding agent]
- Reference website URL(s): [paste URL(s), if any]
- Reference screenshots/assets: [available files, if any]
- Pages/routes to improve or recreate: [list, or identify the main flow]
- Primary users and tasks: [who uses it and what they need to do]
- Preferred visual direction: [optional]
- Constraints: [framework, APIs, deadline, browser support, etc.]

PHASE 1 — INSPECT BEFORE EDITING
- Read project instructions and inspect Git status, framework, routes, components, styles, assets, API/data contracts, authentication, permissions, and tests.
- Preserve unrelated and uncommitted changes. Do not reset or overwrite user work.
- If a reference URL is provided, inspect the accessible pages before coding. Review full-page structure, navigation, section order, content density, typography, spacing, colors, borders, shadows, image crops, icons, sticky elements, hover/focus states, forms, menus, dialogs, and motion.
- Inspect representative desktop, tablet, and mobile widths. Record observed facts separately from assumptions. If the browser/reference is inaccessible, state that limitation and use only the evidence I supplied—never pretend you inspected it.

PHASE 2 — PLAN THE RECREATION OR IMPROVEMENT
- Map reference pages and shared components to the existing project architecture.
- Define reusable design tokens for color, typography, spacing, radii, shadows, breakpoints, and interaction states.
- List the largest visual and UX gaps, planned file changes, risks, and acceptance criteria.
- Prioritize overall structure and proportions first, then typography/color, assets, interactions, responsive behavior, and micro-details.
- Do not pause for minor unknowns. Make reasonable, reversible assumptions and note them.

PHASE 3 — IMPLEMENT WITH HIGH FIDELITY
- Reuse the existing stack and components where practical. Avoid a needless rewrite or dependencies without a clear reason.
- Recreate the reference's key layout, spacing, hierarchy, typography, color roles, component shapes, media composition, navigation, and meaningful motion as closely as available evidence supports.
- Use assets supplied by me or assets authorized for reuse. If an asset is unavailable, create an original substitute and disclose it; do not pretend it is the original asset.
- Implement working navigation and controls—not decorative dead buttons. Forms, filters, tabs, menus, dialogs, and other in-scope interactions must behave correctly.
- Preserve existing business logic, APIs, database schema, routes, authentication, authorization, and data contracts unless I explicitly approve changes.
- Build real loading, empty, validation, success, failure, disabled, and permission states where relevant. Do not fake a backend success if the service is not connected.
- Make the interface work at narrow, medium, and wide widths. Include keyboard navigation, visible focus, semantic markup, readable contrast, and prefers-reduced-motion support.

PHASE 4 — COMPARE, REFINE, VERIFY
- If browser/screenshot tooling is available, capture the reference and local implementation at equivalent viewport sizes.
- Compare side by side, list the five most consequential differences, fix them, and repeat. Check the whole page—not just the hero or first viewport.
- Run available lint, typecheck, tests, build, and relevant browser checks. Inspect console/network errors, overflow, broken assets, and core user flows.
- Review the final diff and fix regressions. Do not claim checks passed unless they were actually run.

FINAL REPORT
- Summarize the user-facing improvements and reference patterns reproduced.
- List exact files and routes changed.
- State which reference pages and viewports were actually inspected.
- Report real test/build/browser results.
- Disclose unavailable assets, inaccessible pages, assumptions, backend dependencies, and remaining visual differences.

BOUNDARIES
Do not bypass login, paywalls, anti-bot protections, or access restrictions. Do not collect private data or build deceptive credential-capture pages. Use original implementation code and only authorized assets. Never claim pixel-perfect fidelity without actual comparison evidence.

START
Inspect the workspace and reference first, then carry the implementation through to a verified, usable result. Do not stop at a plan, a list of suggestions, or a static mockup.
```

## Reference Website Recreation

A URL alone is not enough to guarantee a faithful recreation. Interface Craft Pro uses an evidence-led workflow:

| Stage | What the agent investigates |
|---|---|
| Reference inspection | Accessible pages, full-page sections, navigation, responsive layouts, and key states |
| Design extraction | Typography, spacing, color roles, grids, surfaces, image composition, and design tokens |
| Interaction mapping | Menus, forms, filters, tabs, dialogs, sticky behavior, and transitions |
| Project mapping | Existing routes, components, APIs, data models, and constraints |
| Iterative implementation | Structure first, then styling, assets, behavior, responsive details, and motion |
| Visual comparison | Side-by-side screenshots at equivalent sizes when tooling is available |
| Verification | Core flows, accessibility, responsiveness, tests, build, and honest limitations |

The goal is **high visual and behavioral fidelity supported by evidence**. Results depend on the pages and assets that can actually be inspected, the tools available, and the scope of the task. The skill does not promise pixel-perfect results without comparison.

## Capabilities

<table>
  <tr><th>Capability</th><th>What it helps deliver</th></tr>
  <tr><td><strong>Existing UI/UX improvement</strong></td><td>Audit and improve a live codebase while preserving business behavior and integrations.</td></tr>
  <tr><td><strong>Reference-driven recreation</strong></td><td>Systematically inspect and reproduce page structure, visual language, responsive behavior, and interactions.</td></tr>
  <tr><td><strong>Design systems</strong></td><td>Consistent design tokens, reusable components, typography, spacing, color, and surfaces.</td></tr>
  <tr><td><strong>Operational interfaces</strong></td><td>Dashboards, tables, filters, forms, admin panels, empty states, and error recovery.</td></tr>
  <tr><td><strong>Interaction and motion</strong></td><td>Purposeful transitions, meaningful control states, and reduced-motion alternatives.</td></tr>
  <tr><td><strong>Accessibility and responsive design</strong></td><td>Keyboard usability, visible focus, semantic structure, contrast, and layouts across screen sizes.</td></tr>
  <tr><td><strong>Verification</strong></td><td>Practical checks, screenshot comparisons where available, and an honest final report.</td></tr>
</table>

## Repository Structure

| Path | Purpose |
|---|---|
| `SKILL.md` | Main instructions and end-to-end workflow |
| `references/website-replication-playbook.md` | Reference inspection, design extraction, implementation passes, comparison, and fidelity scorecard |
| `references/` | Design foundations, hierarchy, responsive layouts, typography, accessibility, forms, interactions, motion, and performance |
| `integrations/` | Optional resources and fallback strategies |
| `templates/` | Reusable audit, implementation-plan, and final-review templates |
| `examples/` | Example briefs for dashboards, landing pages, and complex animation |
| `tests/` | Skill quality checks and evaluation scenarios |

## Engineering Principles

- Inspect before editing; protect existing work.
- Preserve business logic and data contracts.
- Recreate from observed evidence, not guesses.
- Prioritize visual structure and usability before decorative effects.
- Prefer authorized assets and original implementation code.
- Make controls functional and states intentional.
- Verify actual behavior and report limitations clearly.

## License and Third-Party Materials

No repository-wide license is declared in this release. Public visibility alone does not grant reuse rights. Add an explicit license before broad redistribution. External references and third-party assets remain subject to their own terms.
