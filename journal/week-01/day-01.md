# Week 01 / Day 01 — Dataset Intelligence & Experiment Design

**Date:** 2026-11-16  
**Status:** Planned; no task marked complete  
**Project:** [Classical ML Fraud Detection](../../projects/01-classical-ml/README.md)

## Mission
Design a defensible, reproducible experiment for severely imbalanced transaction fraud classification **before** training sophisticated models.

## Learn (explain in your own words)
- Binary classification and positive-class prevalence
- Why accuracy is misleading under imbalance
- Precision, recall, F1, PR-AUC, ROC-AUC
- Train/validation/test responsibilities and leakage risks

## Implement
- [ ] Establish project environment, data acquisition instructions and source manifest
- [ ] Inspect schema, rows, missing values, duplicates, class counts and Time/Amount distributions
- [ ] Write an experimental protocol (split, preprocessing, metrics, baselines, seed, test isolation)
- [ ] Commit reproducible dataset analysis scripts (no raw dataset committed)

## Evaluate
- [ ] Quantify class imbalance from observed counts
- [ ] Explain expected behavior of a majority-class baseline
- [ ] Document assumptions and limitations of the dataset

## Technical defense (without AI answers)
1. With 0.2% fraud prevalence, what accuracy does an all-negative classifier achieve, and why is it useless?
2. How can fitting a scaler before data splitting leak information?
3. When would a chronological split be preferred over a random stratified split?
4. Why is PR-AUC useful for evaluating rare-event classifiers?

## Observed commands and outputs
_Not yet run._

## Decisions and reasoning
_Not yet recorded._

## Failures, misconceptions, corrections
_Not yet recorded._

## Evidence / commit references
_Not yet available for ML tasks._

## Day 1 acceptance gate
- [ ] Dataset provenance and integrity documented
- [ ] Class imbalance measured from actual dataset
- [ ] Experimental design with leakage controls committed
- [ ] All four defense questions answered in own words

## Next
After verification, begin Day 02: split, preprocessing and leakage tests.
