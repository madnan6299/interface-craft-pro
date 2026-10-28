# Premium Design Directions: Landing Pages, Motion, and Workflow Builders

Use this guide when the user wants a premium marketing site, visually ambitious landing page, high-craft UI, or node-based workflow editor. The reference sites are research inputs, not assets or code sources to copy.

## Direction selector

Choose a named direction based on the product's primary job. A project may combine directions, but declare one primary direction and explain any secondary influence.

| Keyname | Best fit | Visual/interaction signature | Avoid |
|---|---|---|---|
| `uberdesigner-premium-landing` | Product launches, SaaS marketing, agencies, portfolios, editorial landing pages | Strong hero composition, confident typography, purposeful whitespace, distinctive section rhythm, curated media, clear CTA, consistent page-wide art direction | Generic hero + three-card template, copied paid templates, invented social proof |
| `horizonx-immersive-motion` | Creative technology, AI products, premium product storytelling, visual portfolios | Original 3D/WebGL or shader visuals when justified, scroll chapters, layered depth, interactive visual components, refined transitions, high-contrast art direction | Motion for its own sake, heavy effects on every section, inaccessible text, unbounded GPU/CPU use |
| `reactflow-workflow-canvas` | Workflow automation, agent builders, process maps, visual editors, node-based tools | Pan/zoom canvas, legible nodes and edges, clear handles, contextual toolbars, selection/validation states, minimap/controls where useful, keyboard and touch support | Decorative diagrams mistaken for functional editors, unclear connectors, hidden controls, canvas-only navigation |
| `material-enterprise-control-center` | ERP, CRM, admin panels, hosting dashboards, operational software | Calm neutral surfaces, layered navigation, semantic color, information density, reusable controls, clear status and error recovery | Every element inside a card, low-contrast labels, arbitrary gradients/glows |
| `editorial-product-story` | Brand storytelling, case studies, creative portfolios, premium service pages | Art-directed type, deliberate content pacing, large visual moments, asymmetric but controlled grids, clear narrative | Poor readability, long scroll with no wayfinding, visual novelty that obscures the offer |

## 1. UberDesigner Premium Landing

Reference: https://uberdesigner.ai/

The useful pattern is a prompt-to-implementation discipline paired with curated landing-page craft. Treat each reference as a structured design specification, not as a screenshot to imitate blindly.

### Inspect
- Hero message, headline line breaks, supporting copy, CTA hierarchy, media placement, and first-screen balance.
- Header/navigation density, section order, content width, grid rhythm, backgrounds, image treatments, and footer.
- The page's distinctive idea: a single strong visual or composition that makes it recognizable without copying its brand.
- How the design remains coherent across every section, including secondary pages and mobile.
- CTA destinations, form behavior, hover/focus, loading, validation, and success/error states.

### Implement
- Write a concise art-direction statement before coding: audience, promise, emotional tone, visual motif, typography character, palette, and motion level.
- Build the entire narrative: hero, evidence/proof only when real, product explanation, benefits, use cases, objections/FAQ when useful, and a clear close.
- Use deliberate typography scale and line length. Hand-tune wrapping only where it improves hierarchy without breaking responsive behavior.
- Use original or authorized imagery. If unavailable, create original art with a consistent composition and disclose substitutions.
- Deliver real responsive HTML/components, functional links/forms, metadata, accessible landmarks, and polished focus states—not just a hero mockup.

### Acceptance criteria
- The first viewport communicates what it is, who it is for, and the next action.
- Section order and art direction feel intentional and coherent.
- Desktop and mobile both feel designed rather than resized.
- No fake testimonials, metrics, customer logos, or dead CTAs.
- Compare screenshots at equivalent widths where browser tooling is available.

## 2. HorizonX Immersive Motion

Reference: https://horizonx.so/

The useful pattern is production-minded visual ambition: a strong visual concept, original interactive assets, and motion integrated into the story. Recreate principles with original work; do not copy paid assets, proprietary code, or protected template files.

### Choose the right rendering level
1. Static/CSS composition for lightweight depth, gradients, masks, and simple transitions.
2. SVG/canvas for crisp vector or controlled particle effects.
3. Three.js/WebGL/shaders only when real-time depth, lighting, particles, or 3D interaction materially improves the concept.
4. Scroll animation libraries only when the project already uses them or the choreography justifies a dependency.

### Motion specification
For every major effect, record:
- Purpose: what it explains, emphasizes, or helps the user explore.
- Trigger: load, pointer, click, scroll, or a meaningful state change.
- Duration/easing and end state.
- Interruption and cleanup behavior.
- Reduced-motion alternative.
- Performance budget and static fallback.

### Implementation rules
- One signature visual is usually stronger than many competing effects.
- Keep headings, navigation, CTAs, and essential information readable and available if WebGL fails.
- Prefer transform/opacity for ordinary transitions; avoid continuous expensive rendering when the scene is idle.
- Respect `prefers-reduced-motion`, mobile thermal/battery constraints, touch input, and lower-powered devices.
- Provide a fallback poster or CSS composition when WebGL/canvas is unsupported.
- Do not lock scrolling, delay the primary CTA, or hide essential content behind a long animation.
- Check contrast over imagery, focus visibility, keyboard operation, and mobile layout.

### Acceptance criteria
- Motion has a clear purpose and feels consistent with the brand.
- The page stays responsive and usable without motion.
- No persistent console errors, broken scene, severe jank, or inaccessible content.
- The experience degrades gracefully on touch devices and reduced-motion settings.

## 3. React Flow Workflow Canvas

Reference: https://reactflow.dev/ and https://reactflow.dev/examples

Use this direction for interfaces in which users create, inspect, or operate relationships between steps. React Flow is a reference for node-editor interaction patterns; it is not a mandate to use that library in every framework.

### Canvas architecture
- Separate the canvas, node palette, contextual inspector, top actions, minimap/zoom controls, and optional execution/log panel.
- Keep node layout readable with a consistent grid, alignment, spacing, and connector routing.
- Each node should communicate its type, title, key configuration, state, and connection affordances.
- Differentiate source/target handles, valid connection previews, invalid connections, selected nodes, disabled nodes, and runtime errors.
- Use edge labels and status markers only where they clarify data or execution flow.

### Required interactions
- Pan, zoom, fit-to-view, select, move, connect, reconnect, and delete where applicable.
- Add nodes through a discoverable palette or contextual insertion.
- Validate connections before committing them; explain why an invalid connection is rejected.
- Provide node configuration in an inspector or dialog with validation and preserved input.
- Support undo/redo and save/restore when the product's scope requires them.
- Confirm destructive bulk operations and show the number of affected nodes/edges.
- Provide keyboard alternatives for key actions and touch-friendly controls.
- Treat execution status as a real state from the engine; never fake a successful run.

### UX states
- Empty canvas with a clear first-step action.
- Node hover, selected, focused, dragging, invalid connection, and disabled states.
- Unsaved changes, saving, save failure, validation failure, running, succeeded, failed, and cancelled execution states where relevant.
- Large-graph handling: contextual zoom, minimap, viewport culling/virtualization where supported, and clear selection feedback.
- Responsive fallback: on small screens, prioritize node configuration and task lists; do not assume a large desktop canvas can simply shrink.

### Acceptance criteria
- Users can understand where a flow starts, how it connects, and where it ends.
- Connection meaning remains clear at normal zoom and dense graphs remain navigable.
- All visible controls work and execution states reflect actual backend results.
- Keyboard, focus, touch, zoom, and error recovery are tested.

## 4. Material Enterprise Control Center

Reference within this repository: `material-inspired-enterprise-ui.md`.

Use for ERP/CRM/admin tasks where scanability, density, permissions, and reliability matter more than cinematic visuals. Keep global navigation, contextual navigation, and the main work area distinct; use semantic tokens, restrained elevation, readable tables, and explicit operational states.

## Combining directions

- Marketing site for an AI workflow product: `uberdesigner-premium-landing` as primary, `horizonx-immersive-motion` as a limited secondary influence, and `reactflow-workflow-canvas` only for product screenshots or the actual editor.
- Automation builder: `reactflow-workflow-canvas` as primary, Material enterprise patterns for settings/inspector panels, restrained motion for transitions.
- ERP/hosting dashboard: `material-enterprise-control-center` as primary. Use premium landing patterns only on public marketing pages.
- Creative portfolio: `editorial-product-story` or `horizonx-immersive-motion` depending on whether narrative or real-time visual interaction is the core experience.

Never apply a direction solely because it looks impressive. Optimize for the user's job, existing product identity, accessibility, maintainability, performance, and real content.

## Reference evidence and rights
- Inspect public pages, routes, interactions, and responsive behavior using available tools. Do not claim inspection of inaccessible areas.
- Keep an evidence log separating observed facts, interpretation, and assumptions.
- Use screenshots as layout evidence; use original code and authorized assets.
- Paid galleries, template downloads, Figma files, private assets, and source archives are not implicitly licensed for copying.
- The `blob:` URLs created inside browser-based apps are session-local and cannot be reliably opened as public reference URLs. Ask the user to upload the underlying screenshot/image or provide a normal HTTPS URL.
