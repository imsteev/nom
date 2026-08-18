---
name: principle-less-is-more
description: Apply when choosing a solution shape, refactoring, or tempted to add code. Reach the outcome with the least total code and indirection. Subtract before adding. Prefer deletion.
disable-model-invocation: true
---

# Less is more

Do the thing with the least amount of code. Subtract before you add. Prefer deletion.

## Decision rule

1. State the required outcome.
2. Delete obsolete paths, duplicated decisions, and unused flexibility first.
3. Add only the mechanism the remaining outcome needs.
4. Judge the total system after the change, not the number of lines in the diff.

Do not minimize line count by hiding complexity, weakening the model, or pushing work onto callers. Clear, explicit code can be the smaller system.

## Failure signals

- The new path ships beside the old path.
- A helper, wrapper, option, or compatibility layer adds indirection without deleting a decision elsewhere.
- The change preserves speculative flexibility no current requirement uses.

## Boundary

This principle judges the final system. **Minimum change necessary** judges the scope of the current change. **High premium on platform** wins only when a shared capability or invariant has earned a common owner.
