---
name: principle-minimum-change
description: Apply when scoping a fix or feature. Change only what the requested outcome requires. Pressure-test every hunk by removing it. Separate independently justified structural preparation from the behavior change.
disable-model-invocation: true
---

# Minimum change necessary

If a fix hinges on a change to one part, do not change anything else, unless there is a structural reason to do so. Pressure test what is needed from the original implementation by progressively removing code.

## Decision rule

For every changed hunk, ask: if I remove this hunk, does the requested outcome still hold? If yes, remove it.

A structural change is necessary only when the direct patch would duplicate an invariant, violate ownership, admit an invalid state, or make the requested behavior unsafe. Isolate that preparation as a behavior-preserving, verifiable unit. Do not use it to admit adjacent cleanup.

## Failure signals

- Drive-by renames, formatting, comments, or "while I'm here" cleanup share the behavior diff.
- Reverting the requested behavior would also revert unrelated improvements.
- The rationale for a hunk is "cleaner" rather than necessary for the outcome.

## Boundary

This is not a smallest-diff-at-any-cost rule. **First principles thinking** can expose a structural prerequisite. **Sequence changes in verifiable units** keeps that prerequisite separate. **Less is more** judges the resulting system.
