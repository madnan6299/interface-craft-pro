# Example: Complex Animation Task

## Goal
Use motion to explain a state transition or story without delaying the user's task.

## Plan
1. Define the trigger, user purpose, sequence, and final state.
2. Check whether CSS or framework-native motion is enough.
3. Use GSAP only if timeline orchestration or scroll sequencing materially helps.
4. Keep semantic content available before and after the animation.
5. Add reduced-motion behavior and component cleanup.
6. Test interruption, route changes/unmount, touch input, and low-motion settings.

## Acceptance
- Motion has a clear purpose and can be skipped or reduced.
- No essential action waits for decorative movement.
- Timelines/listeners/observers are cleaned up.
- No unsupported plugin or API is assumed.
- Actual verification is documented.
