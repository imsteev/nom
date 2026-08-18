---
name: principle-make-change-easy
description: Apply when the current shape would bury the real diff. Sequence behavior-preserving refactors that would make the main change extremely clear and focused. Relies on Less is more and Minimum change necessary.
disable-model-invocation: true
---

# Make it easy to make a change

Sequence behavior-preserving refactors that would make the main change extremely clear and focused. Rely on Less Is More, Minimum Change Necessary principles.

**When.** The current shape would bury the real diff. A behavior change that is simple after a move, extract, or deletion, and muddy before it.

**Skipped-it tell.** One commit that both reshapes the code and changes behavior. A reviewer cannot tell which hunks are the bug.

**Related.** This is the Core triad's first move when zooming out found a structural reason. The refactor commit preserves behavior. The next commit is Minimum change necessary. Less is more still applies to what remains after both land.
