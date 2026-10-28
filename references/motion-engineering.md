# Motion Engineering

Motion is an interface behavior with engineering costs, not decoration by default.

## Choose the least complex tool
1. CSS transition/keyframes for simple hover, focus, and state changes.
2. Framework-native transitions for component lifecycle or route changes.
3. GSAP for coordinated timelines, complex sequencing, scroll-linked scenes, or when its control model is genuinely useful.
4. No motion when it does not improve understanding.

Do not add a dependency solely to animate a simple opacity or transform change.

## Specify each motion
For each meaningful animation define:
- Trigger and user intent.
- What the movement communicates.
- Duration and easing.
- Initial and final states.
- Interruption/cancellation behavior.
- Reduced-motion alternative.
- Cleanup requirements.

## Performance
Prefer `transform` and `opacity` for frequent animation. Avoid repeatedly animating layout-heavy properties unless justified. Avoid scroll handlers that do expensive work on every frame; use suitable observers or animation libraries and clean them up. Ensure timelines, event listeners, observers, and contexts are reverted or killed when components unmount.

## Accessibility and usability
- Respect `prefers-reduced-motion: reduce`.
- Never delay an essential action for decorative motion.
- Avoid forced scroll hijacking and unnecessary parallax.
- Ensure content and controls remain available if animation fails.
- Consider touch devices, lower-powered hardware, and reduced network conditions.

## GSAP integration notes
Use the project's installed GSAP version and official API documentation. Do not assume a plugin is installed or licensed. Scope selectors to the component, use context/cleanup patterns supported by the installed version, and verify cleanup after remounts. Avoid global selectors that animate unrelated parts of the page.

## Baseline CSS example
```css
.interactive {
  transition: transform 160ms ease, opacity 160ms ease;
}
.interactive:hover {
  transform: translateY(-1px);
}
@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after {
    scroll-behavior: auto !important;
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
  }
}
```

Apply broad reduced-motion rules carefully in real products; preserve essential state changes and test the result.
