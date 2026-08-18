---
name: principle-minimum-change
description: Apply when a fix or feature seems to want a wide edit. If a fix hinges on a change to one part, do not change anything else, unless there is a structural reason to do so. Pressure test what is needed by progressively removing code.
disable-model-invocation: true
---

# Minimum change necessary

If a fix hinges on a change to one part, do not change anything else, unless there is a structural reason to do so. Pressure test what is needed from the original implementation by progressively removing code.

**When.** A fix or feature that seems to want a wide edit.

**Skipped-it tell.** Drive-by renames, comment churn, or "while I'm here" cleanups in the same diff as the fix. The tell after the fact is a revert that has to unwind unrelated files.

**Related.** The structural reason comes from zooming out under First principles thinking. Pay that reason with Make it easy to make a change, not by mixing it into the behavior diff. Less is more judges the end state, not how wide this commit is.
