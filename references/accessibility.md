# Accessibility Baseline

Treat accessibility as part of implementation, not a final cosmetic pass. This checklist is a practical baseline, not a claim of formal WCAG conformance.

## Semantics and names
- Use native elements for their intended purpose: buttons for actions, links for navigation, labels for form controls.
- Maintain a logical heading hierarchy and meaningful landmarks.
- Every input has a programmatic label; placeholders are examples, not labels.
- Icon-only controls have accessible names and visible tooltips where appropriate.
- Images have useful alternative text when informative and empty alt text when decorative.

## Keyboard and focus
- All interactive functionality is keyboard operable.
- Focus order follows the task flow and visible focus is never removed without a replacement.
- Do not create keyboard traps. Dialogs manage focus on open/close and support expected escape behavior.
- Do not make hover the only way to reveal an important action.

## Feedback and errors
- Associate validation messages with their fields and describe how to fix the problem.
- Preserve valid user input after recoverable errors.
- Announce important async status updates appropriately without excessive live-region chatter.
- Do not rely on color alone for errors, status, or selection.

## Motion and media
- Honor `prefers-reduced-motion` and provide a reduced or instant alternative for nonessential movement.
- Avoid flashing effects and unnecessary continuous motion.
- Ensure content remains understandable if animation or media fails.

## Practical verification
Use keyboard-only navigation, zoom, narrow viewports, browser accessibility tools, and automated checks where available. Automated tools do not replace manual review. Report the checks performed and any known gaps; do not claim certification without a formal, scoped assessment.
