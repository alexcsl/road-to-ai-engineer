# Week 05 — NLP — tokenization, transformers and evaluation design
**Planned start:** 2026-12-14 · **Project:** `projects/03-nlp-llm/` · **Status:** Planned syllabus, not actual progress
**Weekly result:** A licensed multilingual NLP dataset, held-out benchmarks, interpretable baseline and transformer training plan.

## Daily curriculum

### Day 01 — Problem and dataset
- **Learn:** Classification/extraction vs generation, label taxonomy, multilingual distribution.
- **Implement:** Choose focused Indonesian-English financial-document NLP task and licensed labeled data; document annotation or synthetic source limitations.
- **Experiment/evaluate:** Check label balance, duplicates, document provenance, train/eval contamination.
- **Defend independently:** Why must document-related chunks be grouped?
- **Pass when:** Dataset protocol and held-out split with contamination checks.

### Day 02 — Text preprocessing
- **Learn:** Unicode, casing, tokenization, subword OOV behavior.
- **Implement:** Build normalization and whitespace/regex baseline; inspect tokenizer artifacts.
- **Experiment/evaluate:** Measure token-length distribution and truncation effects.
- **Defend independently:** Show BPE subword example and tradeoffs.
- **Pass when:** Tokenizer analysis saved and reproducible.

### Day 03 — Classical NLP baseline
- **Learn:** TF-IDF, sparse vectors, linear models.
- **Implement:** Train TF-IDF + logistic baseline with train-only vocabulary.
- **Experiment/evaluate:** Measure per-label F1, macro/micro scores and confusion matrix.
- **Defend independently:** When is TF-IDF stronger than embeddings?
- **Pass when:** Reproducible baseline and label-wise error analysis.

### Day 04 — Transformer internals
- **Learn:** Embeddings, attention Q/K/V, masking, positional signals.
- **Implement:** Trace tiny self-attention tensor example; inspect pretrained encoder architecture and shapes.
- **Experiment/evaluate:** Numerically verify attention output dimensions/normalization.
- **Defend independently:** Calculate attention weights and masked softmax unaided.
- **Pass when:** Documented attention walkthrough and tests.

### Day 05 — Pretrained model baseline
- **Learn:** Pooling, classification heads, batching, max token length.
- **Implement:** Evaluate small multilingual encoder zero-shot where valid or pretrained feature baseline; define fair comparator.
- **Experiment/evaluate:** Compare latency/quality to TF-IDF, with same held-out split.
- **Defend independently:** Why does pretraining help small datasets?
- **Pass when:** Transformer baseline results with fair setup.

### Day 06 — Error taxonomy
- **Learn:** Language distribution, domain shift, label ambiguity.
- **Implement:** Audit failure slices: Indonesian vs English, rare terms, long documents, OCR noise.
- **Experiment/evaluate:** Record hand-inspected errors and revised hypotheses without test leakage.
- **Defend independently:** Propose 2 plausible interventions and expected tradeoffs.
- **Pass when:** Error taxonomy and next-week fine-tuning plan.

### Day 07 — NLP week audit
- **Learn:** Evaluation reliability and compute feasibility.
- **Implement:** Freeze dataset/split, config and baselines; prepare PEFT plan, retrospective.
- **Experiment/evaluate:** Reproduce evaluation; inspect license and contamination.
- **Defend independently:** Explain attention, tokenization and macro F1 without AI.
- **Pass when:** Week 5 baselines and Week 6 hypothesis approved.

## Weekly integration gate
- Demonstrate and reproduce: A licensed multilingual NLP dataset, held-out benchmarks, interpretable baseline and transformer training plan.
- Link actual commands, configs, runs, tests, failures and independent defense in this week's journal.
- Apply [universal quality gates](../docs/QUALITY_GATES.md), record unresolved issues, and update [sprint progress](../SPRINT_PROGRESS.md).
- Next week starts only after required evidence or explicit documented exception; do not manufacture completion.
