---
name: principle-platform-premium
description: Apply when a stable capability or invariant belongs below multiple features. Put complexity in a well-owned generic and keep call sites simple. Syntactic duplication alone does not earn an abstraction.
disable-model-invocation: true
---

# High premium on platform

We care about the underlying generics and primitives. Powerful abstractions; simple call sites.

## Admission test

Build a shared abstraction only when all are true:

- Multiple features need the same capability or invariant, not merely similar syntax.
- The shared owner can expose a smaller, more stable contract than its callers.
- Centralizing the behavior removes policy or coordination from call sites.
- The abstraction can be tested without knowing any one product feature.

A second caller is evidence, not proof. Do not predict generic requirements from hypothetical callers.

## Failure signals

- A "platform" helper has one caller or encodes that caller's nouns.
- Options accumulate so each caller can recover behavior the abstraction hid.
- The shared layer imports a feature to finish its work.
- Call sites stay as complex as before.

## Boundary

**Less is more** wins for one-off behavior. **Dependencies point inwards** places the shared owner below its consumers. **Type system fundamentalist** keeps its contract simple.
