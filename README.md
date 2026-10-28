# ✦ Interface Craft Pro

<p align="center">
  <strong>Turn an existing interface into a polished, usable product — without breaking the app.</strong>
</p>

<p align="center">
  A self-contained UI/UX engineering skill for AI coding agents. Audit first. Improve what matters. Verify the result.
</p>

<p align="center">
  <a href="#-quick-start">Quick Start</a> ·
  <a href="#-copy-paste-prompt">Copy-Paste Prompt</a> ·
  <a href="#-what-it-improves">What It Improves</a> ·
  <a href="#-how-it-works">How It Works</a>
</p>

---

## 🚀 Quick Start

**Already have a project? You do not need to rebuild it from scratch.**

1. **Make this repository available to your AI coding agent** using its supported skill/import method. If it has no repository skill support, provide `SKILL.md` as project instructions and keep this repository accessible.
2. **Open your existing project** in the agent (for example, Cursor, Codex, Claude Code, or another coding agent that can inspect and edit project files).
3. **Copy the prompt below**, paste it into the agent, fill in the small project details, and run it.

> **Important:** Visiting or starring this GitHub repository does not automatically install the skill into your coding agent.

## 📋 Copy-Paste Prompt

Copy everything in this prompt into your coding agent while your existing project is open.

```text
Act as a senior UI/UX engineer and use Interface Craft Pro as your implementation playbook.

GOAL
Improve the UI/UX of my EXISTING application so it feels polished, consistent, intuitive, responsive, accessible, and production-ready. Improve the actual project—not just produce a design concept or mockup.

PROJECT DETAILS
- App/product: [briefly describe it]
- Main screen or workflow: [specific page, route, or feature; or audit the whole app in prioritized phases]
- Main users: [customers, admins, warehouse staff, accountants, etc.]
- Known issues / desired style: [optional]
- Non-negotiable constraints: [optional]

NON-NEGOTIABLE SAFETY RULES
- Inspect the repository instructions, file structure, current Git status, framework, existing design system, routes, components, APIs, data models, authentication, permissions, and tests BEFORE editing.
- Preserve existing business logic, API contracts, database schema, authentication, authorization, routes, and working features unless I explicitly approve a change.
- Never overwrite or discard unrelated or uncommitted work. Do not perform destructive changes.
- Do not rewrite the whole application or add dependencies without a clear, justified need.
- Keep the current stack and conventions where practical. Reuse existing components and design tokens; improve them consistently instead of adding one-off styles everywhere.

WORKFLOW
1. AUDIT: Inspect the real code and user flow. Identify visual inconsistencies, confusing hierarchy, poor spacing, typography/color issues, responsive problems, inaccessible controls, dead interactions, and missing loading/empty/error/success states.
2. PRIORITIZE: Rank issues by impact. Share a concise diagnosis, proposed direction, files likely to change, risks, and acceptance criteria. Then proceed when the scope is clear—do not ask unnecessary questions.
3. IMPLEMENT: Fix the highest-impact issues in coherent steps. Make real controls work. Improve layout, visual hierarchy, feedback, forms, navigation, and relevant interaction states. Avoid superficial decoration that harms clarity.
4. ACCESSIBILITY & RESPONSIVENESS: Support keyboard navigation, visible focus, semantic structure, readable contrast, form labels and useful validation. Check narrow, medium, and wide layouts. Respect prefers-reduced-motion.
5. VERIFY: Run the checks available in this project, such as lint, typecheck, tests, build, and browser/manual checks. Review the final diff. Fix regressions you find.
6. REPORT HONESTLY: Summarize improvements, list exact files changed, report checks actually run and their results, and disclose remaining limitations. Never claim a test passed if it was not run.

RESOURCE FALLBACK
Read SKILL.md first, then use only the relevant bundled guides under references/, templates/, integrations/, and tests/. External tools, libraries, websites, and slash commands are optional—not required. If one is unavailable, use the bundled guidance and continue without pretending it was used.

START NOW
Inspect the existing project, audit the requested screen/workflow, and improve the real implementation. Do not stop after giving advice or creating a static mockup. Preserve existing functionality and verify your changes.
```

## ✨ What It Improves

| Area | Practical outcome |
|---|---|
| Visual hierarchy | Clearer page structure, emphasis, spacing, and readability |
| Responsive UI | Better behavior across mobile, tablet, and desktop |
| Design consistency | Reusable patterns, typography, colors, and components |
| Forms & feedback | Better validation, helpful errors, and clear success states |
| Dashboards & data tables | More usable admin screens, filters, empty states, and dense data |
| Accessibility | Keyboard support, focus states, semantics, and contrast |
| Motion & interaction | Purposeful transitions without distracting or excessive animation |
| Performance | Practical guidance for keeping interfaces responsive |
| Safe changes | Protects existing business logic and contracts while improving the UI |

## 🧭 How It Works

<details>
<summary><strong>1. Inspect before changing</strong></summary>

The agent examines the existing app, its conventions, Git status, UI components, routes, and important contracts before editing.
</details>

<details>
<summary><strong>2. Fix the biggest UX problems first</strong></summary>

It prioritizes broken or risky behavior, major usability issues, accessibility gaps, inconsistent patterns, and then optional polish.
</details>

<details>
<summary><strong>3. Implement real, usable improvements</strong></summary>

It aims for working interactions and complete states—not just attractive screenshots or dead buttons.
</details>

<details>
<summary><strong>4. Verify and report</strong></summary>

It runs available project checks, reviews changes, and clearly reports what was and was not verified.
</details>

## 🧰 What's Included

- **`SKILL.md`** — the main entry point and end-to-end engineering workflow.
- **`references/`** — portable guidance for design foundations, hierarchy, responsive layouts, typography, accessibility, forms, dashboards, landing pages, motion, and performance.
- **`integrations/`** — optional external resources and fallback strategies.
- **`templates/`** — reusable audit, implementation-plan, and final-review templates.
- **`examples/`** — examples for dashboards, landing pages, and complex animation tasks.
- **`tests/`** — skill quality checks and evaluation cases.

You can start with the prompt above; the agent should consult the relevant repository guides as needed. You do **not** need to read every reference file manually first.

## 💡 Tips for Better Results

- Name the exact route or workflow you want improved.
- Explain who uses it and what they need to accomplish.
- Mention what must not change (for example, API behavior or permissions).
- For a large application, improve one high-value workflow at a time.
- Share screenshots or design references when available.
- Ask the agent to verify interactions—not just visual appearance.

## 🔒 Design Principles

- Preserve functionality while improving usability.
- Prefer clear, consistent design over decoration for decoration's sake.
- Make loading, empty, error, success, disabled, and permission states intentional.
- Treat external resources as optional and verify their current availability and license before reuse.
- Be honest about tests, limitations, and what was actually changed.

## 📄 License & Reuse

No repository-wide license is declared in this release. Public visibility alone does not grant permission to reuse the repository's contents. Choose and add an explicit license before broad redistribution; third-party resources retain their own terms.
