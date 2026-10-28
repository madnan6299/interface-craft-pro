# Interface Performance

## Goals
Keep the interface responsive under realistic data, network, and device conditions. Measure before making speculative optimizations.

## Practical rules
- Avoid unnecessary dependencies and duplicate UI libraries.
- Use appropriately sized images, modern formats where supported, and lazy loading for below-the-fold media.
- Reserve media dimensions to reduce layout shift.
- Avoid expensive work during render and repeated state updates that do not affect visible output.
- Keep animation work lightweight and avoid layout thrashing.
- Use pagination, virtualization, or server-side filtering when actual dataset size requires it.
- Show useful loading feedback for operations that take noticeable time; avoid skeletons for every tiny action.
- Treat errors and slow responses as normal product states.

## Verification
Run the project's existing build, lint, tests, and performance checks when available. Inspect browser console and network failures. Compare before/after measurements when performance is the stated goal. Do not promise specific speed gains without measurements.
