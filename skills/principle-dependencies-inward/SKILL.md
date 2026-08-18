---
name: principle-dependencies-inward
description: Apply when choosing module ownership, adding an import, or breaking a cycle. Stable policy must not know volatile product or infrastructure details. Move shared knowledge to its owner or invert the edge.
disable-model-invocation: true
---

# Dependencies point inwards

Dependencies point toward the module that owns the invariant. Generic modules must not import product-specific callers. Stable policy must not import volatile UI, storage, transport, or framework details.

Always ask: "should A know about B?"

## Decision rule

When adding an edge:

1. Name the knowledge the edge carries.
2. Put that knowledge in the module that owns the invariant.
3. Pass a value when the consumer needs a result, not the producer.
4. Invert the dependency with an interface or callback when policy must invoke a detail.
5. Add a mediator only when coordination is a real domain responsibility.

A cycle proves ownership is unresolved. A lazy import, event bus, or service locator can hide the cycle without resolving it.

## Failure signals

- A core or generic module imports a feature, UI, or adapter.
- A transport or storage type leaks into domain logic.
- Two modules know each other's private representations.
- A cycle disappears only because resolution moved to runtime.

## Boundary

**High premium on platform** decides when shared capability deserves a lower common owner. **Your model is your world** defines the invariants dependencies should point toward.
