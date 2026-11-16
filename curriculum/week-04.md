# Week 04 — Computer vision — transfer learning, localization and serving
**Planned start:** 2026-12-07 · **Project:** `projects/02-deep-learning-cv/` · **Status:** Planned syllabus, not actual progress
**Weekly result:** A justified pretrained CV model comparison, appropriate localization experiment and inspectable inference demo.

## Daily curriculum

### Day 01 — Transfer learning baseline
- **Learn:** Feature reuse, frozen backbone vs fine-tuning, normalization contracts.
- **Implement:** Train pretrained ResNet/EfficientNet head on same training split.
- **Experiment/evaluate:** Compare validation metrics, time and parameters to custom CNN.
- **Defend independently:** When should frozen layers be unfrozen?
- **Pass when:** Comparable transfer baseline with architecture rationale.

### Day 02 — Fine-tuning strategy
- **Learn:** Discriminative learning rates, batchnorm, schedules, mixed precision.
- **Implement:** Unfreeze selected layers; implement staged training and early stopping.
- **Experiment/evaluate:** Compare frozen vs tuned performance and compute cost.
- **Defend independently:** Explain batchnorm behavior under transfer.
- **Pass when:** Staged run reproducible; no validation peeking into test.

### Day 03 — Localization choice
- **Learn:** Classification vs detection vs anomaly localization; mAP/IoU.
- **Implement:** Inspect dataset annotation availability; select lightweight detection/localization OR document why impossible.
- **Experiment/evaluate:** Establish correct metric baseline and qualitative samples.
- **Defend independently:** How does IoU differ from classification accuracy?
- **Pass when:** Justified task/model decision; no fabricated bounding boxes.

### Day 04 — Training & hard examples
- **Learn:** NMS, thresholds, confidence and annotation quality if detection used.
- **Implement:** Train/evaluate selected localizer or robust anomaly baseline.
- **Experiment/evaluate:** Analyze FP/FN, object sizes/background slices and annotation limitations.
- **Defend independently:** Why can mAP hide critical operational failures?
- **Pass when:** Task-appropriate eval and failure report.

### Day 05 — Inference packaging
- **Learn:** Transforms parity, device selection, batching and export.
- **Implement:** Implement local FastAPI image inference and stable preprocessing.
- **Experiment/evaluate:** Compare predictions on direct model vs API fixed fixtures.
- **Defend independently:** Why can train/serve preprocessing mismatch destroy accuracy?
- **Pass when:** Tested service and input validation.

### Day 06 — Optimization
- **Learn:** ONNX/quantization choices, latency-memory-quality tradeoffs.
- **Implement:** Optional ONNX export if supported; benchmark native CPU vs alternative.
- **Experiment/evaluate:** Collect p50/p95 latency and memory on fixed hardware, compare output agreement.
- **Defend independently:** Explain quantization accuracy/latency limits.
- **Pass when:** Measured report; unsupported optimization explicitly deferred.

### Day 07 — CV project audit
- **Learn:** Integration, reproducibility, visual failure demo.
- **Implement:** Clean install/tests; record model, eval protocol, artifacts and Week 4 retrospective.
- **Experiment/evaluate:** Frozen final test once if not already used; check examples and release constraints.
- **Defend independently:** Independently debug shape error and architecture choice.
- **Pass when:** Project 02 releasable evidence or documented blockers.

## Weekly integration gate
- Demonstrate and reproduce: A justified pretrained CV model comparison, appropriate localization experiment and inspectable inference demo.
- Link actual commands, configs, runs, tests, failures and independent defense in this week's journal.
- Apply [universal quality gates](../docs/QUALITY_GATES.md), record unresolved issues, and update [sprint progress](../SPRINT_PROGRESS.md).
- Next week starts only after required evidence or explicit documented exception; do not manufacture completion.
