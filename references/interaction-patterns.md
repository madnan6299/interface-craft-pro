# Interaction Patterns

## Buttons and links
- Label actions with verbs and specific outcomes.
- Distinguish primary, secondary, quiet, and destructive actions.
- Prevent accidental duplicate submissions where appropriate and show progress while an action is pending.
- Links navigate; buttons change state or submit an action. Avoid fake links and dead controls.

## Forms
- Group fields by task and keep labels visible.
- Mark required fields clearly and explain non-obvious formats before submission.
- Validate at the right time: lightweight feedback while editing, full validation on submit, and authoritative validation on the server.
- Associate errors with fields, summarize larger form failures, and preserve entered data when possible.
- Disable submit only when the reason is understandable; never make an inaccessible disabled state the only explanation.

## Dialogs, menus, and popovers
- Use dialogs for focused decisions or tasks, not as a container for entire applications.
- Support expected keyboard behavior, focus management, dismissal, and small-screen sizing.
- Keep menu item labels clear and do not hide critical workflows in ambiguous overflow menus.

## Async states
Every async workflow should define pending, success, failure, and retry behavior as appropriate. Prevent duplicate requests when necessary. Explain whether a failure lost, saved, or preserved the user's changes.

## Destructive actions
Explain the consequence, identify the target, and request confirmation when the action is difficult to reverse. Prefer undo or recovery where practical. Never make destructive action the default.

## Micro-feedback
Use immediate feedback for selection, toggles, save state, copying, and validation. Feedback should be proportional: a subtle state change for a toggle, a concise status message for a completed task, and a clear recovery path for failure.
