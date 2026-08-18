# Bug fix

**Own the mechanism. Reproduce, isolate, fix, and prove.**

Every shipped line must trace to evidence. A defensive change that might help is a hypothesis, not a fix.

1. State the expected behavior, actual behavior, and shortest known reproduction.
2. Reproduce the defect on the same path the user experiences. Capture the failing state before changing code.
3. Form competing root-cause hypotheses. Run the smallest experiment that distinguishes them. Instrument unclear state instead of guessing.
4. Confirm the failing mechanism. If it cannot be reproduced or isolated, report the result as inconclusive and do not ship a speculative fix.
5. Add the cheapest regression check that fails for the confirmed mechanism. Keep a manual reproduction when an automated check would test the wrong layer.
6. Design the smallest root-cause fix. Use **First principles thinking** only when the current shape causes the defect. Separate any behavior-preserving preparation with **Sequence changes in verifiable units**.
7. Implement the fix. Remove disproven experiments, temporary instrumentation, speculative guards, and unrelated cleanup.
8. Run the original reproduction on the same path. Run focused tests, then the broader checks justified by the blast radius.
9. Inspect the diff against **Minimum change necessary**. Sequence the failing reproduction before the fix when the repository's delivery model allows it.

**Reply:** what was broken, the confirmed root cause, the fix, and comparable failing-then-passing evidence.
