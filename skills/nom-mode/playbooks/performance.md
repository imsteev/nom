# Performance

**Own the measurement story. Do not optimize from source alone.**

Use for measured slowness, excess resource use, throughput limits, or latency regressions where the requested deliverable includes an improvement.

1. Define the metric, workload, environment, and target. A vague report of slowness must become a repeatable measurement.
2. Capture a baseline with enough repetitions to distinguish signal from noise.
3. Profile or instrument the real workload. Identify the dominant cost before proposing a fix.
4. Form hypotheses from the evidence. Consider deleting work first, then a better data structure or index, batching, caching with explicit invalidation, reduced I/O, deferred or rescheduled work, and safe parallelism. Try only strategies supported by the measurement.
5. Make one focused change. Measure it with the same workload and method before trying another. Revert changes that do not improve the target.
6. Verify correctness on the real path. Account for memory, load, consistency, startup, and tail-latency tradeoffs introduced by the optimization.
7. Add a regression check when the metric can be measured reliably in automation.
8. Report the baseline, result, absolute and relative delta, measurement method, and remaining bottleneck. An inconclusive result is not a win.

**Reply:** the baseline, dominant cost, chosen fix, comparable post-change result, tradeoffs, and evidence location.
