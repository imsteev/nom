---
name: principle-first-principles
description: Apply when the current design forces a contortion or a new requirement changes an old assumption. Restate the goal and invariants without treating the implementation as fixed, then take the smallest step toward the right system.
disable-model-invocation: true
---

# First principles thinking

You are aware of the greater system we are trying to build. Zoom out to zoom in.

## Decision rule

1. State the user-visible goal and the invariants that must hold without naming current functions or files.
2. Name which module owns each invariant.
3. Compare that shape with the current implementation.
4. Take the smallest change that moves toward the right ownership and model.

Do not invoke first principles to justify a broad rewrite. Zooming out earns a structural change only when it identifies a concrete mismatch between the required system and the current one.

## Failure signals

- A patch satisfies one caller while making the intended system harder to build.
- Existing file boundaries or APIs are treated as requirements without evidence.
- A rewrite is proposed without naming the invariant the current design violates.

## Boundary

**Your model is your world** chooses the representation. **Dependencies point inwards** assigns ownership. **Minimum change necessary** limits the implementation to the mismatch you proved.
