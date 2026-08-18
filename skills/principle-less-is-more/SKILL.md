---
name: principle-less-is-more
description: Apply when refactoring, sizing a diff, or tempted to add code. Do the thing with the least amount of code. Subtract before you add. Prefer deletion.
disable-model-invocation: true
---

# Less is more

Do the thing with the least amount of code. Subtract before you add. Prefer deletion.

**When.** Refactoring, sizing a diff, or tempted to add code.

**Skipped-it tell.** An addition that leaves the old path in place. A helper extracted before anything was deleted. A "small" wrapper that exists to avoid touching the caller.

**Related.** Minimum change necessary is about the diff against HEAD. This is about the end state. High premium on platform loses unless the generic is the work or already has a second caller.
