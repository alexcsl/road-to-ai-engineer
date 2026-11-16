# Week 03 — Deep learning — PyTorch mechanics and CNN baseline
**Planned start:** 2026-11-30 · **Project:** `projects/02-deep-learning-cv/` · **Status:** Planned syllabus, not actual progress
**Weekly result:** Independently explain tensor operations and gradients and train a custom CNN on a public image dataset.

## Daily curriculum

### Day 01 — Vision task & data audit
- **Learn:** Image tensors, shape conventions, normalization, target definitions.
- **Implement:** Select public defect/visual anomaly dataset with license; inspect class counts, image sizes, group/batch splits.
- **Experiment/evaluate:** Check duplicates/near-duplicates, leakage via same physical object, data quality.
- **Defend independently:** Trace RGB image HWC -> BCHW; justify split.
- **Pass when:** Data provenance, group-aware evaluation protocol, class/task metrics.

### Day 02 — Autograd from first principles
- **Learn:** Chain rule, computational graphs, gradient accumulation.
- **Implement:** Implement small tensor operation gradient check and linear layer forward/backward; compare autograd.
- **Experiment/evaluate:** Finite difference gradient check and numeric tolerance.
- **Defend independently:** Derive dL/dW for a linear layer.
- **Pass when:** Correct gradient checks, learner implements one derivative unaided.

### Day 03 — CNN design
- **Learn:** Convolution, padding, stride, receptive field, pooling, parameter count.
- **Implement:** Implement custom small CNN, print tensor shapes, loss, optimizer and config.
- **Experiment/evaluate:** Test output dimensions for odd/even sizes; validate forward/backward finite values.
- **Defend independently:** Compute output shape and trainable parameters manually.
- **Pass when:** CNN architecture documented; shape tests pass.

### Day 04 — Training loop
- **Learn:** Batches, augmentation, learning rate, optimizer, weight decay.
- **Implement:** Write training/validation loop with deterministic seed, logging, checkpoint logic.
- **Experiment/evaluate:** Small overfit-one-batch sanity check then proper baseline training.
- **Defend independently:** Why should tiny-batch overfit work? Explain optimizer steps.
- **Pass when:** Loss decreases in sanity test; baseline run logged.

### Day 05 — Regularization and diagnostics
- **Learn:** Overfitting, dropout, augmentations, class weights, data shift.
- **Implement:** Compare a small set of train-only augmentations and regularization changes.
- **Experiment/evaluate:** Train-vs-val curves, per-class recall/confusion, control seeds.
- **Defend independently:** Why can augmentation hurt?
- **Pass when:** Controlled comparison and failure modes documented.

### Day 06 — Baseline robustness
- **Learn:** Label errors, corruption sensitivity, duplicate detection.
- **Implement:** Inspect misclassifications; test blur/brightness/rotation or realistic corruption variants.
- **Experiment/evaluate:** Report per-slice performance and identify systematic failures.
- **Defend independently:** Propose mitigation without modifying test.
- **Pass when:** Error analysis with visual examples that respect dataset license.

### Day 07 — Defense & integration
- **Learn:** Reproducibility and engineering quality.
- **Implement:** Run clean training/evaluation pipeline and retrospective; document architecture.
- **Experiment/evaluate:** Re-run baseline with saved config; test model load and deterministic eval.
- **Defend independently:** Implement minimal train step unaided, explain gradients/layers.
- **Pass when:** CNN baseline verified; >=8/10 defense; Week 3 gate.

## Weekly integration gate
- Demonstrate and reproduce: Independently explain tensor operations and gradients and train a custom CNN on a public image dataset.
- Link actual commands, configs, runs, tests, failures and independent defense in this week's journal.
- Apply [universal quality gates](../docs/QUALITY_GATES.md), record unresolved issues, and update [sprint progress](../SPRINT_PROGRESS.md).
- Next week starts only after required evidence or explicit documented exception; do not manufacture completion.
