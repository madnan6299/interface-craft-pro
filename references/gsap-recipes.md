# GSAP Recipes (Guidance, Not a Dependency)

Use GSAP only if installed and justified. Check installed version and project conventions before relying on APIs.

## Timeline pattern
1. Scope selectors to the component/page instance.
2. Sequence only meaningful elements.
3. Prefer transform/opacity for frequent animation.
4. Keep content readable before and after the sequence.
5. Clean up timelines, triggers, listeners, and contexts on teardown.
6. Provide reduced-motion behavior and test re-entry/re-render.

## Scroll-trigger pattern
Use only when it improves spatial understanding. Do not hijack scrolling, delay access to content, or create duplicate triggers after remount. Test short viewports, touch, and reduced motion.

Avoid adding GSAP for a simple hover effect or assuming an API exists without checking the installed version. If absent, use CSS or the framework's existing transitions.