# Visual Hierarchy and Layout

## Page composition
1. Establish page context with a concise title and, when useful, a short explanation.
2. Place the primary action where users expect it and keep it visually distinct.
3. Use consistent alignment edges for titles, filters, tables, and content groups.
4. Keep related controls together; separate unrelated groups.
5. Use whitespace to indicate structure. Add borders or surfaces only when they improve grouping.

## Typography
- Use a deliberate type scale with clear roles for page title, section heading, body, label, helper text, and metadata.
- Keep body text comfortably readable and line lengths manageable.
- Avoid using tiny, low-contrast text to force more content into a view.
- Reserve bold weight for hierarchy, not every label.
- Use tabular numerals for aligned financial and operational figures when supported.

## Color and contrast
- Assign colors semantic roles and use them consistently.
- Never communicate status by color alone; include text, icon, or another cue.
- Test contrast for text, icons, borders, focus indicators, and disabled states.
- Keep decorative color subordinate to the task.

## Tables and data-heavy views
- Make column labels clear and align values consistently; right-align numeric columns where that improves scanning.
- Preserve table context on small screens using an intentional responsive strategy: horizontal scroll with cues, prioritized columns, or a suitable alternate layout.
- Provide empty, loading, failure, and no-results states.
- Make row actions discoverable without hiding essential actions behind hover-only behavior.
- Filters should show applied state and offer a clear reset path.
- Use pagination or virtualization when data size justifies it; do not add complexity preemptively.

## Cards and dashboards
- A card needs a reason to exist: grouping, summary, action, or comparison.
- Avoid making every element a card. Combine open layout, dividers, and surface changes.
- Metrics should include a meaningful label and, when relevant, timeframe or comparison context.
- Charts need a title, understandable units, and a useful empty state.

## Responsive checks
Review narrow mobile, medium/tablet, and wide desktop layouts. Check navigation, sticky elements, tables, dialogs, long labels, zoom, and keyboard focus. Do not rely on one fixed viewport or a single screenshot.
