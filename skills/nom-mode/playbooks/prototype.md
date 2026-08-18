# Prototype

**Own the decision, not production code.**

Use a prototype to answer an empirical design or behavior question cheaply. The deliverable is a decision backed by observation. If the desired behavior is already known, route directly to Feature.

1. State the single decision the prototype must make and the observation that will decide it.
2. Choose the cheapest artifact that can produce that observation. Keep it isolated from production source and state.
3. Build only the alternatives needed to expose the tradeoff. Use two or three variants when comparison matters. Skip production abstractions, migrations, polish, and comprehensive tests.
4. Exercise the artifact on the matching surface. Capture screenshots for visual differences, video for motion, output for behavior, and measurements for timing.
5. Compare the alternatives against the decision criterion. Make a recommendation, including a no-build result when none earns production work.
6. Treat the artifact as throwaway. Carry the chosen behavior, constraints, and evidence into Feature. Do not promote prototype structure into production by default.

**Reply:** the decision tested, alternatives, observed evidence, recommendation, and scratch artifact location. State plainly that the prototype is not production code.
