---
name: principle-dependencies-inward
description: Apply when wiring layers, imports, or a cycle. Low level abstractions must not depend on higher level ones. A cycle needs a mediator or an inversion. Always ask whether A should know about B.
disable-model-invocation: true
---

# Dependencies point inwards

Low level abstractions must not depend on higher level ones. If there is a cycle, that indicates a mediator is necessary, or a way to invert using techniques like dependency injection. Always ask: "should A know about B?"

**When.** Wiring layers, imports, or a cycle.

**Skipped-it tell.** A core module that imports a feature, UI, or adapter. A cycle you "fixed" with a lazy import. A knows about B when only B needed a result from A.

**Related.** High premium on platform keeps generics below features. Your model is your world is the inward core those dependencies should point at.
