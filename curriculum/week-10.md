# Week 10 — MLOps — reproducibility, data/model versioning, CI and operations
**Planned start:** 2027-01-18 · **Project:** `04-document-intelligence` · **Status:** Planned syllabus, not actual progress
**Weekly result:** A reproducible AI engineering release pipeline with versioned data/config/model artifacts, automated checks and operational visibility.

## Daily curriculum

### Day 01 — Artifact lineage
- **Learn:** Experiment IDs, model versions, dataset hashes, reproducibility.
- **Implement:** Audit all projects for versions/seeds; implement manifests for key models, retrieval index and datasets.
- **Experiment/evaluate:** Reproduce one baseline experiment and compare recorded metrics.
- **Defend independently:** Why is code hash alone insufficient?
- **Pass when:** Artifact lineage evidence and documented gaps.

### Day 02 — Experiment tracking
- **Learn:** MLflow or equivalent, checkpoints, run comparisons.
- **Implement:** Integrate tracking for training and evaluation configs without leaking secrets.
- **Experiment/evaluate:** Check metric parity and reproducible rerun from config.
- **Defend independently:** What makes an experiment reproducible?
- **Pass when:** Tracking run linked to exact inputs.

### Day 03 — Quality gates and CI
- **Learn:** Unit/integration/test isolation, fast smoke jobs, caching.
- **Implement:** Implement GitHub Actions lint, tests and minimal smoke without private data/secrets.
- **Experiment/evaluate:** Trigger CI on sample change, inspect failure reporting.
- **Defend independently:** What should CI avoid doing with final test data?
- **Pass when:** CI verified from an actual run or explicitly pending.

### Day 04 — Serving versions
- **Learn:** Model registry ideas, deployment configuration, rollback.
- **Implement:** Version model/index dependencies, expose version in responses, document rollback.
- **Experiment/evaluate:** Test mismatched index/model pair behavior.
- **Defend independently:** What makes model rollback different from ordinary code rollback?
- **Pass when:** Version compatibility tests and rollback instructions.

### Day 05 — Data quality and drift
- **Learn:** Feature/embedding distributions, data drift vs concept drift.
- **Implement:** Define monitoring schema with synthetic/safe sample telemetry; no sensitive logs.
- **Experiment/evaluate:** Test schema shift, empty documents and language skew.
- **Defend independently:** Why might drift signals not imply model failure?
- **Pass when:** Monitoring plan and drift checks with limitations.

### Day 06 — Operations reliability
- **Learn:** Timeouts, retries, queues, graceful degradation.
- **Implement:** Add health probes, structured logs, safe retry policy and bounded concurrency.
- **Experiment/evaluate:** Simulate upstream failure and delayed response.
- **Defend independently:** When should an agent abstain versus retry?
- **Pass when:** Failure-injection evidence and runbook.

### Day 07 — Week 10 reproducibility audit
- **Learn:** Supply-chain security, licenses, deployability.
- **Implement:** Perform lockfile/dependency/secret audit and end-to-end clean setup; retrospective.
- **Experiment/evaluate:** Validate CI, training artifacts, sample requests and negative tests.
- **Defend independently:** Reproduce a known failure and explain fix unaided.
- **Pass when:** Operational reproducibility gate satisfied or blocked.

## Weekly integration gate
- Demonstrate and reproduce: A reproducible AI engineering release pipeline with versioned data/config/model artifacts, automated checks and operational visibility.
- Link actual commands, configs, runs, tests, failures and independent defense in this week's journal.
- Apply [universal quality gates](../docs/QUALITY_GATES.md), record unresolved issues, and update [sprint progress](../SPRINT_PROGRESS.md).
- Next week starts only after required evidence or explicit documented exception; do not manufacture completion.
