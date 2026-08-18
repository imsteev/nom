---
name: principle-type-system
description: Apply when designing or reviewing types. Use the simplest type that excludes consequential invalid states. Do not add type machinery for precision or one caller.
disable-model-invocation: true
---

# Type system fundamentalist

Use the simplest type definitions possible. Do not do type gymnastics just to satisfy a single call site. Make illegal states unrepresentable with that same simple construction.

## Decision rule

1. Model the domain before choosing the type syntax.
2. Identify invalid combinations that would cause a real bug.
3. Choose the simplest construction that prevents those combinations.
4. Parse untrusted data at the boundary, then trust the type inside.
5. Keep matches exhaustive when variants carry different behavior.

Do not brand every primitive, encode every refinement, or strengthen a collection unless interchange or partiality is a real risk. Precision has a carrying cost.

If one caller needs type gymnastics, adapt the caller or fix the model. Do not distort a shared type around one use site.

## Failure signals

- A bag of optionals admits contradictory combinations.
- A cast or "should never happen" check compensates for a weak model.
- A conditional type, mapped type, or wrapper stack exists for one caller.
- The type is more precise than any operation requires.

## Boundary

**Your model is your world** chooses the representation. This principle encodes it with the compiler. **High premium on platform** does not excuse a contract only one caller can use.
