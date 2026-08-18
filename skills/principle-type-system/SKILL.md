---
name: principle-type-system
description: Apply when designing or reviewing types. Use the simplest type definitions possible that make illegal states unrepresentable. Do not do type gymnastics just to satisfy a single call site.
disable-model-invocation: true
---

# Type system fundamentalist

Use the simplest type definitions possible. Do not do type gymnastics just to satisfy a single call site. Make illegal states unrepresentable with that same simple construction.

**When.** Designing or reviewing types.

**Skipped-it tell.** A bag of optionals that admits nonsense combinations. Or a conditional type, mapped type, or four-layer wrapper that exists to please one caller.

**Related.** Your model is your world picks the structure. This is how that structure is typed. Gymnastics for one call site means the model is wrong or the caller should adapt. High premium on platform does not excuse a type that only one caller can inhabit.
