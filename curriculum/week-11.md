# Week 11 — Optimization — model serving, performance and reliability
**Planned start:** 2027-01-25 · **Project:** `04-document-intelligence` · **Status:** Planned syllabus, not actual progress
**Weekly result:** An honest performance, cost and reliability report with measured optimizations and documented regressions.

## Daily curriculum

### Day 01 — Benchmark design
- **Learn:** Warmup, p50/p95, throughput, memory, hardware controls.
- **Implement:** Define fixed query workloads (short/long, languages, concurrent users); build load harness.
- **Experiment/evaluate:** Capture baseline latency/throughput/memory and error rate.
- **Defend independently:** What invalidates cross-hardware performance comparisons?
- **Pass when:** Repeatable benchmark method and baseline captured.

### Day 02 — Inference batching and caching
- **Learn:** Batch throughput vs latency, cache keys and staleness.
- **Implement:** Implement one justified cache/batching variant.
- **Experiment/evaluate:** Measure p50/p95 latency and stale-result correctness risk.
- **Defend independently:** When can caching make quality/security worse?
- **Pass when:** Controlled A/B run with correctness checks.

### Day 03 — Model/runtime optimization
- **Learn:** Quantization, model sizes, serving options and precision.
- **Implement:** Choose feasible ONNX/quantized/efficient inference candidate, or document infeasibility.
- **Experiment/evaluate:** Measure accuracy/quality change, memory, latency under same workload.
- **Defend independently:** Why can quantization reduce quality or sometimes slow CPU workloads?
- **Pass when:** Empirical quality-performance tradeoff report.

### Day 04 — Retrieval/index optimization
- **Learn:** Index parameters, batch embedding, storage/index costs.
- **Implement:** Optimize one measured retrieval bottleneck without changing evaluation protocol.
- **Experiment/evaluate:** Compare quality and p95 retrieval time, index build cost.
- **Defend independently:** Can approximate nearest neighbor decrease recall?
- **Pass when:** Retrieval optimization benchmark with regression checks.

### Day 05 — Failure and load tests
- **Learn:** Backpressure, concurrency limits, timeouts, circuit breakers.
- **Implement:** Exercise simultaneous requests, malformed inputs, upstream rate limits and recovery.
- **Experiment/evaluate:** Measure failures and graceful degradation, document reproducibility.
- **Defend independently:** What happens when demand exceeds service capacity?
- **Pass when:** Reliability test summary and incident playbook.

### Day 06 — Security + cost review
- **Learn:** Secrets, least privilege, dependencies, per-request cost.
- **Implement:** Review auth, logging, prompt injection, data licensing and deployment spend; optimize one cost driver.
- **Experiment/evaluate:** Report measured token, CPU/GPU and storage usage if available.
- **Defend independently:** How do you prioritize security vs latency?
- **Pass when:** Threat/expense report with residual risks.

### Day 07 — Release benchmark and defense
- **Learn:** Evidence-backed performance claims.
- **Implement:** Freeze configuration, repeat benchmark, publish before/after with raw logs.
- **Experiment/evaluate:** Ensure same test workload, report regressions and uncertainty.
- **Defend independently:** Independently diagnose a latency regression.
- **Pass when:** Week 11 verified report and performance audit.

## Weekly integration gate
- Demonstrate and reproduce: An honest performance, cost and reliability report with measured optimizations and documented regressions.
- Link actual commands, configs, runs, tests, failures and independent defense in this week's journal.
- Apply [universal quality gates](../docs/QUALITY_GATES.md), record unresolved issues, and update [sprint progress](../SPRINT_PROGRESS.md).
- Next week starts only after required evidence or explicit documented exception; do not manufacture completion.
