---
name: principle-model-is-your-world
description: Apply when writing any code, especially stateful or branching. More complicated data models and state lead to more complicated systems. Pick the data structure that avoids kitchen sinks and rigid foundations. Normalization is the default.
disable-model-invocation: true
---

# Your model is your world

More complicated data models and state leads to more complicated systems. Always consider what the right data structure to employ is to avoid kitchen sinks and rigid foundations. Normalization is the default; only denormalize when it starts hurting.

**When.** Any code, especially stateful or branching.

**Skipped-it tell.** A kitchen sink object that grows a field per feature. Or a rigid foundation that forces every new case into the same shape. Denormalized copies that already drift.

**Related.** Type system fundamentalist is how this structure is typed. First principles thinking names the system this model has to serve. Less is more deletes fields and copies this model does not need.
