# Refactoring

**Own the behavior contract. Change the structure, not the behavior.**

Use for renames, moves, extraction, inlining, deduplication, dependency correction, and model reshaping that should preserve observable behavior. Route intentional behavior changes to Feature or Bug fix.

1. State the behavior that must not change.
2. Pin that contract before moving structure. Use a characterization test, baseline output, snapshot, or repeatable real-path check. Compilation alone is not a behavior pin.
3. Name the structural problem and target shape. "Cleaner" is not enough. Point to duplicated knowledge, invalid states, hidden ownership, a dependency violation, unnecessary layers, or another concrete cost.
4. Delete dead paths, redundant wrappers, and unused flexibility before introducing a replacement.
5. Move in the smallest behavior-preserving units. Verify the pin after each unit.
6. Migrate internal callers and delete the old path in the same change. Keep compatibility only for a real external contract.
7. Prove the final behavior against the original pin and the real path.
8. Confirm the result reduced total code, indirection, duplicated knowledge, or invalid states. Revert reshaping that only moved complexity.

**Reply:** the pinned contract, the structural problem, the new shape, the equivalence evidence, and the complexity removed.
