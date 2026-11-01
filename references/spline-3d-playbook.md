# Spline 3D & Interactive Experience Playbook

Use Spline when a real-time 3D or interactive 2D/3D scene improves the user's understanding, product storytelling, or interaction. Spline is an optional production tool—not a required dependency and not a substitute for sound UX.

Official references:
- Spline: https://spline.design/
- Documentation: https://docs.spline.design/
- Getting started: https://docs.spline.design/
- What is Spline: https://docs.spline.design/basics/what-is-spline
- Spline MCP Server: https://docs.spline.design/generate/spline-mcp-server
- Web export: https://spline.design/web
- Viewer export: https://docs.spline.design/exporting-your-scene/web/exporting-as-spline-viewer
- Performance guidance: https://docs.spline.design/

## 1. Decide whether Spline is appropriate

Good fits:
- A hero visual that communicates a physical/digital product.
- Interactive product explainers, configurators, spatial storytelling, and portfolio experiences.
- Original 3D objects, product mockups, diagrams, and lightweight interactive scenes.
- 2D Hana compositions when a designed animated graphic or interface frame is more appropriate than full 3D.

Do not use it by default for:
- Data-heavy ERP/CRM screens, forms, tables, settings, or navigation.
- A decorative scene that competes with the primary CTA or makes text hard to read.
- Pages where the 3D runtime, network cost, or device constraints outweigh the benefit.
- A requirement that can be solved more accessibly and cheaply with CSS, SVG, or a static image.

Before implementation, state: purpose, target users, primary interaction, scene footprint, fallback, and expected performance budget.

## 2. Scene design brief

Create a short scene brief before opening the editor:
- Product/brand context and audience.
- Scene concept and one-sentence story.
- Camera angle, framing, focal object, background, depth, and visual hierarchy.
- Object list with approximate scale and material intent.
- Lighting direction, intensity, environment, and shadow treatment.
- Animation states, triggers, transitions, and final resting state.
- Pointer/touch/scroll/keyboard behavior, if interactive.
- Responsive composition and reduced-motion alternative.
- Target output: Viewer embed, public URL, React/Next.js code export, or self-hosted assets if the account/plan supports it.

Prefer a clear focal object and deliberate composition over many unrelated objects. Use a consistent art direction and the project's existing brand tokens.

## 3. Build and interaction workflow

1. Inspect the existing app, framework, route, styling, asset conventions, and deployment constraints.
2. Create or open the scene in Spline. If Spline MCP is connected, inspect the current file/scene before editing it.
3. Build the scene using original or authorized assets. Keep object names meaningful and organize layers/groups.
4. Define camera and lighting before polishing materials.
5. Add only meaningful interactions: hover/press, drag/orbit, state transitions, scroll response, or data-driven variables where useful.
6. Provide a clear idle state. Animation should settle rather than constantly distract.
7. Preview the scene and capture screenshots at the intended aspect ratios.
8. Export using the smallest appropriate integration surface. Prefer the official Viewer or framework code export documented by Spline.
9. Integrate with a wrapper component that controls dimensions, loading, error, fallback, and accessibility context.
10. Test the full page—not only the Spline editor preview.

Never invent a Spline scene URL. Use only a real URL or exported code supplied by the user or returned by the connected Spline workflow.

## 4. Web integration patterns

### Viewer web component

Spline documents a native `<spline-viewer>` web component for embedding scenes in websites. The current embed package/version and exact snippet should be taken from the Spline export panel or current official documentation, not copied from an old example.

Implementation checklist:
- Load the viewer script once, not once per component instance.
- Avoid adding a second copy of the runtime when the framework export already includes it.
- Keep scene URL in a configuration/env value when it varies by environment.
- Set an explicit responsive container size and stacking context.
- Provide a loading state and a useful static fallback.
- Avoid placing essential text, navigation, or CTAs inside a canvas.
- Confirm content security policy, network access, and deployment restrictions.
- Lazy-load below-the-fold scenes and avoid loading several large scenes at once.

### React / Next.js

- Follow the current Spline export instructions and use the supported React/runtime package only when needed.
- In Next.js, keep browser-only scene initialization inside a client component; dynamically load it when server rendering would otherwise touch browser APIs.
- Avoid duplicate canvas/runtime instances during React Strict Mode remounts.
- Clean up event listeners and scene resources when supported by the selected integration.
- Handle loading, failed network, and component unmount states.
- Do not expose private tokens or secrets in client-side scene variables or code.

### Hosted scene vs self-hosted export

Choose intentionally:
- Hosted public scene/viewer: fastest to iterate, but depends on the external service and network.
- Code export: better source-level integration and control over app lifecycle.
- Self-hosting: use only when the user's Spline plan/export terms support it and the full required runtime/assets are included.

Check licensing, attribution, plan restrictions, and asset rights before shipping. Never assume paid/community assets are free to redistribute.

## 5. Performance budget and fallback

Treat 3D as an enhancement. Set a project-specific budget rather than assuming all devices can run the same scene.

Review:
- Scene complexity, object count, geometry, texture dimensions, texture count, lights, shadows, particles, physics, and animation loops.
- Initial transfer size, number of requests, runtime startup, and time until the primary page content is usable.
- CPU/GPU load, frame stability, memory pressure, thermal impact, and mobile battery.
- Lazy loading, poster/fallback image, and reduced-quality behavior on constrained devices.
- Whether the scene pauses or reduces work when off-screen or not interacting, where supported.

Required fallbacks:
- A static poster or CSS/SVG alternative that preserves the message.
- A no-motion presentation when `prefers-reduced-motion: reduce` is active.
- A clear loading/error state that does not block the rest of the page.
- A functional HTML alternative for any information or action that would otherwise exist only in the 3D scene.

Do not promise a numeric performance result without measuring it on the target devices.

## 6. Accessibility and UX

- Keep primary text and actions in semantic HTML outside the canvas.
- Provide an accessible label/description for the scene and explain its purpose.
- Do not make color the only way to communicate state.
- Ensure keyboard users can reach every essential action without manipulating a 3D object.
- Provide pause/stop or reduced-motion behavior for non-essential continuous animation.
- Avoid disorienting camera movement, flashing, forced perspective changes, or motion that interferes with reading.
- Respect touch input and do not rely on hover-only affordances.
- Make the static fallback understandable, not an empty rectangle.

## 7. Verification checklist

- Scene URL/export is real and loads in the target environment.
- Initial page content and CTA remain usable while the scene loads or fails.
- Desktop, tablet, and mobile framing are checked.
- Keyboard, touch, reduced-motion, and fallback states are checked.
- No overflow, accidental scroll lock, z-index collision, or inaccessible overlay.
- Runtime/network errors are reviewed.
- Performance is measured on representative devices where available.
- Licensing and asset provenance are recorded.
- Screenshots show the integrated page, not only the editor preview.

## 8. Spline MCP and agent collaboration

Spline's official MCP server can allow compatible AI clients to inspect and edit scenes, capture screenshots, and publish when explicitly requested. Availability and setup depend on the user's Spline account, desktop/browser environment, and coding-agent MCP support.

- Read the current official MCP setup guide before configuring.
- Never invent an MCP endpoint, credentials, or configuration schema.
- Ask the user to complete account authorization and connection in their own client when required.
- Use read/inspect operations before making scene edits.
- Keep edits reversible and summarize objects, materials, events, and files changed.
- Do not publish a scene or change sharing permissions unless the user explicitly requests it.
- Do not claim MCP is connected unless a real connection/tool response confirms it.
- If MCP is unavailable, provide a scene brief and exact manual Spline editor steps, then integrate a real exported URL/code when supplied.

## 9. Completion report

Report the scene concept, key objects and interactions, export/integration method, exact project files changed, responsive/fallback/accessibility behavior, checks actually run, and remaining limitations.
