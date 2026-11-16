# Week 02 — Classical ML — inference API, testing and delivery
**Planned start:** 2026-11-23 · **Project:** `projects/01-classical-ml/` · **Status:** Planned syllabus, not actual progress
**Weekly result:** An end-to-end fraud prediction service with validated inputs, versioned artifacts, honest limitations and repeatable deployment.

## Daily curriculum

### Day 01 — Inference contract
- **Learn:** Model serialization risk, schema stability, calibrated outputs.
- **Implement:** Define JSON input/output schemas; version model and preprocessing bundle; provide local inference CLI.
- **Experiment/evaluate:** Compare offline predictions to loaded artifact on fixed fixtures.
- **Defend independently:** What breaks when feature ordering changes?
- **Pass when:** Validated API contract, fixture predictions, serialized version documented.

### Day 02 — FastAPI serving
- **Learn:** Request validation, sync/async CPU inference, error handling.
- **Implement:** Implement /health and /predict with strict feature schema and no raw secrets.
- **Experiment/evaluate:** Test valid, missing, malformed, extreme and unexpected fields.
- **Defend independently:** Explain why CPU-bound inference is not magically async.
- **Pass when:** Endpoint returns schema-compliant results; negative tests pass.

### Day 03 — Security boundaries
- **Learn:** Model artifact trust, serialization risks, data privacy, adversarial inputs.
- **Implement:** Constrain file paths; trust only local artifacts; reject unexpected payloads; redact sensitive logs.
- **Experiment/evaluate:** Probe oversize/malformed values and exception handling; inspect dependency versions.
- **Defend independently:** Why is loading untrusted pickle unsafe?
- **Pass when:** Threat list and meaningful negative tests committed.

### Day 04 — Packaging & environment
- **Learn:** Lockfiles, reproducibility, minimal dependencies.
- **Implement:** Create project packaging/config and Dockerfile, pin dependencies, document exact commands.
- **Experiment/evaluate:** Fresh-environment install, smoke train/infer or artifact smoke test.
- **Defend independently:** What causes environment drift?
- **Pass when:** Build and smoke results recorded; failures explicitly documented.

### Day 05 — API/model performance
- **Learn:** Latency p50/p95, cold/warm loads, throughput and memory.
- **Implement:** Create simple benchmark harness for CPU inference with warmup and controlled concurrency.
- **Experiment/evaluate:** Report environment, batch size, latency distribution and resource use.
- **Defend independently:** Which operations dominate request latency?
- **Pass when:** Benchmark reproduces; no unqualified performance claims.

### Day 06 — Case study + demo
- **Learn:** Experimental communication, model limitation, class-rate shift.
- **Implement:** Write decision records and concise README; expose sample inference workflow/demo.
- **Experiment/evaluate:** Audit metric tables for same split, thresholds, and model versions.
- **Defend independently:** Defend model selection versus dummy and alternatives.
- **Pass when:** A reviewer can run service, inspect honest metrics and limitations.

### Day 07 — Integration review
- **Learn:** Security, test coverage and technical narrative.
- **Implement:** Run clean setup/test/lint/smoke commands; fix P0/P1 problems; publish Week 2 retrospective.
- **Experiment/evaluate:** Evaluate stability on edge fixtures and compare packaged versus notebook outputs.
- **Defend independently:** Explain entire data-to-API path and debug an intentionally wrong input shape unaided.
- **Pass when:** Project 01 release gate met or explicitly blocked with evidence.

## Weekly integration gate
- Demonstrate and reproduce: An end-to-end fraud prediction service with validated inputs, versioned artifacts, honest limitations and repeatable deployment.
- Link actual commands, configs, runs, tests, failures and independent defense in this week's journal.
- Apply [universal quality gates](../docs/QUALITY_GATES.md), record unresolved issues, and update [sprint progress](../SPRINT_PROGRESS.md).
- Next week starts only after required evidence or explicit documented exception; do not manufacture completion.
