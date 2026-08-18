---
name: principle-model-is-your-world
description: Apply when designing state, schemas, or branching logic. Choose one authoritative representation and a data structure that keeps valid changes local. Normalize by default. Denormalize only against measured cost with explicit ownership.
disable-model-invocation: true
---

# Your model is your world

More complicated data models and state lead to more complicated systems. Always consider what the right data structure to employ is to avoid kitchen sinks and rigid foundations. Normalization is the default; only denormalize when it starts hurting.

## Decision rule

Before writing behavior, name:

- The authoritative facts.
- The invariants between them.
- The dominant reads and writes.
- The data structure that makes valid changes local and invalid combinations hard to express.

Keep each fact in one authoritative place. Derive views and indexes. Denormalize only after measuring a read-path cost, then name the owner and synchronization rule for every copy.

Do not force all future behavior through one kitchen-sink object. Do not create a rigid base that requires unrelated cases to share fields or lifecycle.

## Failure signals

- Two fields or stores can disagree about the same fact.
- A new feature adds another boolean that must stay synchronized.
- One object owns unrelated state because it was already convenient to pass around.
- A generic base requires empty, optional, or meaningless fields for some variants.

## Boundary

**Type system fundamentalist** encodes this model statically. **First principles thinking** states the larger system the model serves. **Less is more** removes facts and copies the model does not need.
