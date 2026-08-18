---
name: principle-platform-premium
description: Apply when a generic or primitive is the work, or a second call site already exists. We care about the underlying generics and primitives. Powerful abstractions, simple call sites. Less is more wins for a one-off.
disable-model-invocation: true
---

# High premium on platform

We care about the underlying generics and primitives. Powerful abstractions; simple call sites.

**When.** A generic or primitive is the work, or a second call site already exists.

**Skipped-it tell.** A "platform" helper extracted for one caller. Or the same logic copied at two call sites instead of lifted.

**Related.** Less is more wins for a one-off. Dependencies point inwards. The generic sits below the call sites, not the other way around. Type system fundamentalist keeps that generic's types simple and total.
