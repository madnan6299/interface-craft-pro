# Interface Improvement Task

Read `SKILL.md` and follow the Interface Craft Pro workflow.

## Goal
[Describe the user outcome this interface should improve.]

## Target
- Route/page/component: [path or component]
- Primary user/role: [user]
- Framework and constraints: [stack, compatibility, design system]

## Requirements
- Preserve business rules, API contracts, permissions, and routes unless explicitly asked to change them.
- Inspect before editing; prioritize high-impact UX issues.
- Prefer shared components and tokens over one-off overrides.
- Implement responsive layouts, accessible controls, and complete interaction states.
- Use motion only when it clarifies feedback or spatial relationships.
- Respect `prefers-reduced-motion`.
- Avoid dependencies without a clear benefit.

## Acceptance criteria
- [ ] Primary task is clear and easy to complete.
- [ ] All visible controls have real behavior.
- [ ] Relevant loading, empty, error, and success states are handled.
- [ ] Mobile, keyboard, and reduced-motion behavior are considered.
- [ ] Existing workflows remain intact.
- [ ] Relevant checks/tests/build have run, or blockers are reported.

## Required final report
1. Diagnosis and priorities.
2. Design decisions.
3. Exact files changed.
4. Motion and accessibility notes.
5. Verification actually performed.
6. Remaining limitations or risks.
