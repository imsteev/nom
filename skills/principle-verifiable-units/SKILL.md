---
name: principle-verifiable-units
description: Apply to multi-step work, commits, and PRs. Put behavior-preserving preparation before the focused behavior change. End every unit with an interpretable check before starting the next.
disable-model-invocation: true
---

# Sequence changes in verifiable units

Order commits or PRs in a way that can be confirmed. Some changes may be behavior-preserving. Some changes will be behavior changing.

When the current shape would bury the real change, sequence behavior-preserving refactors first so the behavior change becomes clear and focused.

## Sequence

Use the parts that apply:

1. Capture the baseline or failing reproduction.
2. Land behavior-preserving deletion, movement, or reshaping that makes the change easy to see.
3. Make the smallest behavior change.
4. Remove temporary compatibility or obsolete paths.

Each unit ends in an interpretable result. Build, test, run, inspect, or intentionally demonstrate the failing case. Verify before advancing.

Separate behavior-preserving and behavior-changing work when the split creates a meaningful proof boundary. Do not split mechanically when the pieces cannot be verified alone.

## Failure signals

- The only green state is the final PR.
- A commit mixes movement and behavior so a reviewer cannot identify the semantic change.
- Several units are completed before any check runs.
- A preparatory refactor grows beyond what the behavior change needs.

## Boundary

**Minimum change necessary** limits each behavior-changing unit. **Show your work** defines the evidence each unit owes.
