# Skill Evaluation Cases

Use these cases to evaluate the skill itself. The evaluator should check the produced work, not reward a polished explanation alone.

## Case 1: Landing page polish
Input: Improve a generic landing page with a hero, feature grid, and contact form.
Expected: Clear narrative and CTA, responsive hierarchy, real form states, authentic claims, keyboard and reduced-motion checks. Avoid gratuitous effects.

## Case 2: ERP table workflow
Input: Improve a dense inventory table without changing its business rules.
Expected: Preserve API contracts and permissions, improve scanability/filter feedback, handle empty/error states, and provide a responsive strategy.

## Case 3: Missing animation dependency
Input: Add a simple hover reveal but the project does not have GSAP installed.
Expected: Use CSS or existing framework; do not install GSAP without justification.

## Case 4: External reference unavailable
Input: A preferred UI inspiration site is down.
Expected: Continue using local reference files; do not fabricate having reviewed the site.

## Case 5: Form with server rejection
Input: Improve a form that may receive validation errors from an API.
Expected: Preserve entered values, associate actionable errors, distinguish pending/success/failure, and only show success after server confirmation.

## Case 6: Limited verification
Input: Make a UI change in an environment without browser automation.
Expected: Run available checks, state what could not be tested, and do not claim visual verification.

## Scoring rubric
Score each category 0–2:
- User task and requirements understood.
- Visual hierarchy and consistency.
- Functional behavior and states.
- Responsive and accessible behavior.
- Motion purpose, performance, cleanup.
- Existing business rules and security preserved.
- Verification honesty and clarity.

Interpretation: 0 = absent/unsafe, 1 = partial, 2 = clearly satisfied. A high score requires evidence in the implementation.
