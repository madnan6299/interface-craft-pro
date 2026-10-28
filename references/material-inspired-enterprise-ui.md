# Material-Inspired Enterprise UI

Use this guide when the user asks for a polished admin panel, hosting dashboard, SaaS control center, CRM, ERP, or a visual direction similar to Google Material Design. Treat Material Design as a usability and systems reference—not a requirement to copy Google's product branding or any specific proprietary screen.

## Core goal
Build a calm, highly legible, consistent interface where navigation, hierarchy, surfaces, controls, and feedback feel intentionally designed. Use the user's screenshot as evidence for the requested visual direction, then adapt it to the actual product and existing design system.

## Visual language
- **Clear shell:** separate global/top-level navigation, contextual side navigation, and the active work area. Make the current workspace/site/account and active route easy to identify.
- **Layered surfaces:** use a neutral page canvas, clear navigation surface, and restrained raised panels. Use elevation only to express hierarchy; do not wrap every element in a card.
- **Semantic color:** define primary, on-primary, secondary, surface, surface-container, outline, error, success, warning, and focus tokens. Keep the main action visually distinct. Use accent colors sparingly.
- **Readable typography:** establish consistent roles for page title, section title, body, label, helper text, and metadata. Avoid overly tiny labels and excessive boldness.
- **Consistent geometry:** define spacing, corner radii, control heights, icon sizes, and border thickness as reusable tokens. Do not mix arbitrary radii and spacing values.
- **Meaningful iconography:** use one consistent icon family. Icons should reinforce familiar actions; pair ambiguous icons with text or accessible labels. Do not use emoji as interface icons.
- **Purposeful feedback:** use clear hover, focus, pressed, selected, disabled, loading, success, warning, and error states. Prefer concise inline status banners for important system messages and allow dismissing them only when safe.
- **Dense but calm:** enterprise dashboards can show many functions without visual noise. Use alignment, grouping, dividers, and typographic hierarchy before adding shadows, gradients, or decorative graphics.

## Suggested token baseline
These are starting points, not mandatory values. Adapt to brand, contrast, density, and platform conventions.

| Token | Suggested baseline |
|---|---|
| Page canvas | Very light neutral gray or warm gray |
| Main surface | White or near-white |
| Primary text | Near-black neutral |
| Secondary text | Mid-neutral with tested contrast |
| Outline | Subtle neutral border |
| Primary action | One brand color, reserved for key actions |
| Success / warning / error | Distinct semantic colors plus text or icon |
| Control height | About 36–44 px for desktop controls; larger touch targets on mobile |
| Card radius | Consistent moderate radius, commonly 12–16 px |
| Small control radius | Consistent radius, commonly 8–12 px |
| Spacing rhythm | A consistent 4 px or 8 px base scale |
| Focus ring | Clearly visible and not clipped |

Do not apply these values blindly. Check the existing brand and component library first.

## Dashboard shell composition
1. **Global announcement/admin strip (optional):** use only for genuinely important account, security, or environment notices. Keep the message readable and make its scope clear.
2. **Product top bar:** logo/product identity, current context, and a small number of global actions. Avoid crowding the bar with unrelated promotions.
3. **Primary navigation:** use a compact icon rail only when labels remain discoverable; otherwise use a labeled sidebar. Show active state with more than color alone.
4. **Contextual navigation:** when a selected website, workspace, company, or project has its own sections, visually distinguish this menu from global navigation.
5. **Status/notice region:** reserve predictable space for success, warning, or system messages. Do not let a banner unexpectedly cover navigation or page content.
6. **Main content:** breadcrumb where useful, page title, primary action, then summary/context panels and task-oriented sections.
7. **Responsive fallback:** collapse or transform navigation intentionally on smaller screens. Do not simply squeeze desktop sidebars until labels collide.

## Component guidance
- **Navigation:** consistent icon size, label alignment, active indicator, hover/focus states, and clear group boundaries.
- **Select/search controls:** visible label or clear accessible name, adequate height, keyboard operation, and explicit empty/no-results behavior.
- **Banners:** semantic role, concise message, optional details link, and dismiss control with an accessible name when dismissal is appropriate.
- **Cards/panels:** meaningful grouping, aligned headers, consistent internal padding, and no redundant nested cards.
- **Status chips:** short text and optional icon; never rely on green/red alone.
- **Action buttons:** consistent hierarchy—primary, secondary, tertiary/quiet, and destructive. Avoid multiple equally prominent primary actions in one region.
- **Tables and lists:** align columns, make row actions discoverable, use restrained separators, and preserve usable responsive behavior.
- **Charts and performance widgets:** state what is measured, units/timeframe, last scan or empty state, and next action. Do not invent data.
- **Promotional content:** separate it from core workflows and keep it subordinate to account and task information.

## Screenshot-to-system method
When given a screenshot:
1. Record observable layout regions and their approximate proportions: top strips, navigation rails, sidebars, content canvas, banners, cards, and visible below-the-fold hints.
2. Extract repeated visual rules: spacing, typography, icon family, surface contrast, border/radius, button styles, and active navigation treatment.
3. Separate evidence from assumptions. A cropped screenshot does not prove hidden behavior or the full responsive layout.
4. Translate the observed rules into tokens and reusable components before styling individual sections.
5. Implement the shell and content hierarchy first; refine icon alignment, text baselines, borders, and states afterward.
6. If tools permit, compare local screenshots at the same viewport and correct the largest differences first.
7. Check mobile/tablet separately rather than assuming the desktop composition will scale.

## Accessibility and responsive checks
- Maintain WCAG-appropriate text and non-text contrast; test actual token combinations.
- Provide keyboard access, visible focus, sensible tab order, and accessible names for icon-only actions.
- Ensure navigation active state, system status, and errors are not communicated by color alone.
- Support zoom and long translated labels without clipping.
- Use appropriate touch targets on mobile and avoid hover-only actions.
- Respect reduced-motion preferences and avoid animated banners that distract from tasks.
- Ensure sticky bars and banners do not obscure focus targets or page headings.

## Anti-patterns
- Random gradients, glassmorphism, glow, and shadows added only to make the UI look “modern.”
- Tiny gray labels and low-contrast borders that disappear on common displays.
- Every item rendered as a floating card.
- Emoji used in place of a consistent icon set.
- Icon-only navigation without labels, tooltips, or accessible names.
- Arbitrary spacing, radii, and control heights.
- Banner overload or promotions competing with primary tasks.
- Fake security badges, metrics, scan results, or success states.
- Copying a reference's logo, proprietary assets, or branded visual identity when not authorized.
