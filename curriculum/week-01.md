# Week 01 — Classical ML — data integrity, baselines and evaluation
**Planned start:** 2026-11-16 · **Project:** `projects/01-classical-ml/` · **Status:** Planned syllabus, not actual progress
**Weekly result:** A reproducible, leakage-aware fraud classification experiment with frozen held-out evaluation and an independently defended metric policy.

## Daily curriculum

### Day 01 — Dataset provenance and protocol
- **Learn:** Class prevalence, imbalance, target leakage, PR-AUC versus accuracy.
- **Implement:** Inspect source/licensing; write acquisition manifest, deterministic inspection script, schema and class counts; author experiment protocol.
- **Experiment/evaluate:** Calculate prevalence, missingness, duplicates, feature distributions; draft no-fraud baseline.
- **Defend independently:** Why does 99.8% accuracy potentially detect zero fraud? Explain PR-AUC.
- **Pass when:** Actual dataset report, protocol and source/hash instructions; four Day 1 questions answered.

### Day 02 — Splits and preprocessing
- **Learn:** Temporal vs stratified splits, base-rate drift, imputation/scaling, train-only fit.
- **Implement:** Implement 80/10/10 time split if feasible; validate positive support; compare documented stratified alternative; build sklearn Pipeline.
- **Experiment/evaluate:** Tests: disjoint sets, fit-only-training, no target in features; log label rates and shift.
- **Defend independently:** Can chronological split still leak across unknown cardholders? Why?
- **Pass when:** Deterministic splits and leakage tests pass; limitations recorded.

### Day 03 — Dummy and logistic baseline
- **Learn:** Logits, sigmoid, cross entropy, regularization and decision thresholds.
- **Implement:** Implement DummyClassifier and regularized LogisticRegression with shared fit/evaluate CLI.
- **Experiment/evaluate:** Track validation average precision, ROC-AUC, precision/recall/F1 and confusion matrix.
- **Defend independently:** Derive gradient direction for one misclassified sample; implement sigmoid unaided.
- **Pass when:** Both models reproducibly trained, metrics captured, independent defense recorded.

### Day 04 — Random forest and comparison
- **Learn:** Decision trees, impurity, bagging, generalization.
- **Implement:** Train bounded RandomForest; add comparison table with common split and metrics.
- **Experiment/evaluate:** Compare train-validation gap, runtime and FP/FN examples.
- **Defend independently:** Why can forests learn nonlinearity but overfit?
- **Pass when:** Three candidates compared fairly, overfitting analysis documented.

### Day 05 — Gradient boosting and tuning
- **Learn:** Boosting versus bagging, class weights, controlled hyperparameter search.
- **Implement:** Introduce LightGBM; bounded parameter search using training folds/validation only.
- **Experiment/evaluate:** Record each configuration, runtime, validation AP and class-imbalance effects.
- **Defend independently:** Explain boosting update logic and why test-based tuning invalidates results.
- **Pass when:** Four model families compared with configs, test still sealed.

### Day 06 — Threshold/calibration/ablation
- **Learn:** Ranking versus probability calibration; expected costs; data ablation.
- **Implement:** Pick winning validation model, compare thresholds, perform calibration check and one feature ablation.
- **Experiment/evaluate:** Plot PR/calibration; log assumed FP/FN cost, FP/FN slices, freeze selection.
- **Defend independently:** Why isn't 0.5 optimal? What is an uncalibrated but well-ranked score?
- **Pass when:** Threshold and model frozen; ablation and limitations captured.

### Day 07 — Final test, reproducibility and defense
- **Learn:** Selection bias, final holdout and statistical uncertainty.
- **Implement:** Evaluate frozen model once on test; regenerate all artifacts from clean commands; write Week 1 retrospective.
- **Experiment/evaluate:** Report test AP, ROC-AUC, confusion matrix, selected-threshold metrics and environment.
- **Defend independently:** Reimplement evaluation metrics or confusion matrix unaided; 10-question review.
- **Pass when:** Artifacts reproducible; held-out results preserved; >=8/10 accurate defenses; week gate reviewed.

## Weekly integration gate
- Demonstrate and reproduce: A reproducible, leakage-aware fraud classification experiment with frozen held-out evaluation and an independently defended metric policy.
- Link actual commands, configs, runs, tests, failures and independent defense in this week's journal.
- Apply [universal quality gates](../docs/QUALITY_GATES.md), record unresolved issues, and update [sprint progress](../SPRINT_PROGRESS.md).
- Next week starts only after required evidence or explicit documented exception; do not manufacture completion.
