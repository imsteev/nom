---
name: principle-verifiable-units
description: Apply to multi-step work, commits, and PRs. Order commits or PRs in a way that can be confirmed. Some changes may be behavior-preserving. Some changes will be behavior changing.
disable-model-invocation: true
---

# Sequence changes in verifiable units

Order commits or PRs in a way that can be confirmed. Some changes may be behavior-preserving. Some changes will be behavior changing.

**When.** Multi-step work, commits, PRs.

**Skipped-it tell.** A stack where the only passing state is the last PR. A commit that mixes a behavior-preserving move with a behavior change, so neither can be confirmed alone.

**Related.** Make it easy to make a change puts the preserving units first. Show your work is the confirmation each unit owes. Minimum change necessary keeps each behavior-changing unit small enough to confirm.
