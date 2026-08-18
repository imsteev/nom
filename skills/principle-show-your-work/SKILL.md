---
name: principle-show-your-work
description: Apply when claiming behavior, appearance, or performance changed. Capture comparable before-and-after evidence on the real path. Trust artifacts, not summaries.
disable-model-invocation: true
---

# Show your work

Take screenshots or video recordings when making visual changes. Compare before/after simulations and tests.

## Evidence rule

Match the evidence to the claim:

- Visual change: before and after at the same state, viewport, and interaction point. Use video when motion or timing matters.
- Bug fix: the original reproduction fails before and passes after on the same path.
- Behavior change: compare old and new output for the same input.
- Performance change: compare the same workload and measurement method.
- Delegated work: inspect the diff, artifact, and runtime result. Do not accept the delegate's summary as proof.

Prefer the real product path. A compile, mock, snapshot, or unit test proves only the layer it exercises.

Keep enough evidence for another person to evaluate the claim. Do not record every step when one decisive comparison is enough.

## Failure signals

- "It works" has no artifact.
- Only the after state exists.
- Before and after use different inputs, environments, or measurement methods.
- A test written after the fix was never observed failing against the old behavior.
- The evidence proves a proxy rather than the claimed result.

## Boundary

**Sequence changes in verifiable units** decides when to check. This principle decides what counts as proof.
