# Project 01 — Classical ML Fraud Detection

**Status:** Planned; no trained model or evaluated result yet.

## Goal
Build a reproducible and leakage-aware fraud classification system with interpretable baselines, careful evaluation, and an inference API in Week 2.

**Suggested dataset:** [Credit Card Fraud Detection (ULB/Kaggle)](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud). Access and inspect the original source; record checksum, row counts, license/access constraints and feature schema after download.

## Initial model plan
1. Dummy majority-class baseline
2. Regularized logistic regression
3. Random forest
4. LightGBM

## Evaluation protocol
Prefer a documented chronological train/validation/test strategy where support is sufficient; compare assumptions with stratified splitting. Fit transformations on training data only. Choose models and thresholds on training/validation data; access final test only once after freezing the configuration.

Primary model-ranking metric: **average precision / PR-AUC**; additionally report ROC-AUC, precision, recall, F1, confusion matrices, calibration, and inference cost where applicable. Do not claim observed results before running the experiments.

## Suggested evolution (create folders as needed)
`src/`, `tests/`, `configs/`, `reports/`, `notebooks/`.

## Week 1 Day 1 deliverable
Documented dataset investigation and `reports/experiment_protocol.md`. See [journal](../../journal/week-01/day-01.md).
