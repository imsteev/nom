# Feature

**Own the behavior and the design that supports it.**

Use for new or changed product behavior. Plan in proportion to uncertainty and blast radius. An obvious local change does not need an architecture exercise.

1. State the user-visible outcome, acceptance criteria, and explicit non-goals.
2. Inspect the affected path. Name the current owners, invariants, boundaries, and behavior that must remain.
3. Name the data shape before the logic. Apply **Your model is your world** and **Type system fundamentalist**.
4. Resolve open decisions. Measure or prototype empirical questions. Ask the user only for product intent or preference that evidence cannot decide.
5. Choose the smallest design that satisfies the outcome. Apply **High premium on platform** only when a shared capability passes its admission test.
6. Sequence any necessary behavior-preserving preparation before the focused behavior change. Keep each unit verifiable.
7. Implement the behavior and its focused tests. Avoid compatibility paths, options, and abstractions not required by the acceptance criteria.
8. Exercise the real feature path. Check the full chain from input through state to user-visible output.
9. Review the final diff against **Minimum change necessary** and **Less is more**. Update public contracts or documentation only when behavior exposed to consumers changed.
10. Apply the **unslop** skill to the reply. Read it in full.

**Reply:** what changed for the user, the data shape and design choice, the real-path verification, and any open decision.
