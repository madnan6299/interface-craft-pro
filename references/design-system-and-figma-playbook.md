# Design System and Figma Playbook

This guide turns visual decisions into a maintainable system. Adapt it to the product; it is not a fixed visual theme.

## Design system workflow

1. Inspect current components, tokens, brand guidance, and reference evidence.
2. Identify missing foundations and inconsistencies.
3. Define semantic tokens and component rules before polishing individual screens.
4. Implement one representative screen and review it at target viewports.
5. Expand the system and migrate repeated patterns incrementally.
6. Validate contrast, states, naming, and responsive behavior.

## Token architecture

Use two conceptual layers:
- **Primitive tokens:** raw brand palettes, neutral scales, spacing, radius, typography metrics, elevation, and motion values.
- **Semantic tokens:** role-based aliases such as `surface/default`, `text/primary`, `border/subtle`, `action/primary`, `status/error`, and `focus/ring`.

Components should consume semantic tokens, not raw palette values. Keep light/dark values as modes when the product supports themes. Avoid creating tokens for every one-off value; add tokens for repeated or meaningful roles.

## Typography

Define roles for display, heading, title, body, label, control, and metadata. Choose font family and scale from brand, readability, localization, and project constraints. Maintain clear hierarchy, readable line length, appropriate line height, and consistent weight. Do not force one typeface or a fixed type scale when an established brand system requires otherwise.

## Spacing and geometry

Choose a coherent spacing scale and consistent radii. Apply nested-radius logic only when it improves visual consistency; it is a heuristic, not a mandatory mathematical rule. Define control heights and touch targets appropriate to platform and task. Prefer shared tokens over isolated values.

## Color and contrast

Use semantic roles and test actual foreground/background combinations. Target WCAG 2.2 AA contrast: 4.5:1 for normal text and 3:1 for large text and meaningful UI graphics/boundaries. Never rely on hue alone for status. Use explicit light/dark modes when needed.

## Components

Repeated patterns should become components. Use clear names, variants, and properties. Common interactive variants include default, hover, pressed, focus-visible, disabled, loading, selected, and error as appropriate. Do not create every theoretical combination when the product does not need it. Provide realistic content and representative states.

## Figma workflow (when a Figma tool is available)

- Read the official tool instructions and required Figma skills before API/MCP operations.
- Inspect the file and its libraries before editing.
- Reuse variables, styles, and components; search shared libraries when supported.
- Create or update foundations before screen-level work.
- Use Auto Layout for frames with flowing content and bind dimensions/spacing to variables where supported.
- Organize pages logically (for example Foundations, Components, Screens) without disrupting the user's existing structure.
- Build in small sections and capture screenshots for review.
- Name layers and components meaningfully.
- Ensure component variants cover real states and data views include loading, empty, and error states.
- Check desktop and mobile frames, text wrapping, contrast, focus, and consistency.
- Report exactly what changed and what could not be completed.

Do not assume Figma MCP, a paid feature, a particular plugin, or a specific API method is available. Follow the installed official integration documentation rather than inventing tool calls.
