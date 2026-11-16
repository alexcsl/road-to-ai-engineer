# Week 06 — LLM/NLP — fine-tuning, PEFT and model release
**Planned start:** 2026-12-21 · **Project:** `projects/03-nlp-llm/` · **Status:** Planned syllabus, not actual progress
**Weekly result:** A reproducibly adapted transformer with appropriate comparisons, efficiency measurements and model card.

## Daily curriculum

### Day 01 — Fine-tuning selection
- **Learn:** Full fine-tuning vs LoRA/QLoRA vs encoder head, task/model fit.
- **Implement:** Select appropriately sized model; estimate parameters, VRAM, compute and licenses.
- **Experiment/evaluate:** Compare expected overhead/quality and define measurable experiment.
- **Defend independently:** Why use encoder rather than causal LLM for classification?
- **Pass when:** Model choice justified; hardware budget recorded.

### Day 02 — Training implementation
- **Learn:** Optimizer, scheduler, gradient clipping/accumulation, padding masking.
- **Implement:** Implement dataset collator, fine-tune loop/config with checkpoints.
- **Experiment/evaluate:** Overfit tiny subset sanity test; verify nonzero gradients and masked loss.
- **Defend independently:** Explain what parameters actually update.
- **Pass when:** Training sanity and config proven.

### Day 03 — Adapter training
- **Learn:** LoRA rank/scaling, frozen weights, quantization constraints.
- **Implement:** Run PEFT if compatible; otherwise train task head/small encoder and document why.
- **Experiment/evaluate:** Measure trainable params, time, peak memory and validation quality.
- **Defend independently:** Derive LoRA parameter savings intuitively.
- **Pass when:** At least one valid adapted model with metrics.

### Day 04 — Hyperparameter discipline
- **Learn:** Learning-rate sensitivity, seeds and early stopping.
- **Implement:** Run bounded learning rate or rank/epoch comparison.
- **Experiment/evaluate:** Record training curves, chosen checkpoint and variance if feasible.
- **Defend independently:** Diagnose divergence and catastrophic forgetting.
- **Pass when:** Experimental comparison and clear selection rule.

### Day 05 — Held-out evaluation
- **Learn:** F1/correctness, hallucinations if generation, robustness.
- **Implement:** Evaluate frozen selection on held-out set once; analyze multilingual failure slices.
- **Experiment/evaluate:** Compare fair baseline, latency, memory, and quality.
- **Defend independently:** What does fine-tuning fail to solve?
- **Pass when:** Test report with denominator and limitations.

### Day 06 — Serving & artifacts
- **Learn:** Model weights/adapters, tokenizer versions, inference schema.
- **Implement:** Implement local inference API/CLI; write model card, training reproducibility, licensing notes.
- **Experiment/evaluate:** Check parity between training-eval and served prediction fixtures.
- **Defend independently:** How do adapter and base-model versions interact?
- **Pass when:** Runnable inference and model card.

### Day 07 — Model audit
- **Learn:** Reproducibility, safety and independent defense.
- **Implement:** Clean setup/CPU fallback or limited GPU validation; publish only with authorization/licensing.
- **Experiment/evaluate:** Run tests and report unverified GPU pieces honestly.
- **Defend independently:** Reproduce attention/masking or adapter reasoning independently.
- **Pass when:** Week 6 gate achieved or transparent blocked report.

## Weekly integration gate
- Demonstrate and reproduce: A reproducibly adapted transformer with appropriate comparisons, efficiency measurements and model card.
- Link actual commands, configs, runs, tests, failures and independent defense in this week's journal.
- Apply [universal quality gates](../docs/QUALITY_GATES.md), record unresolved issues, and update [sprint progress](../SPRINT_PROGRESS.md).
- Next week starts only after required evidence or explicit documented exception; do not manufacture completion.
