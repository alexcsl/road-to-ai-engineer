# Week 08 — RAG — hybrid search, reranking and grounded generation
**Planned start:** 2027-01-04 · **Project:** `04-document-intelligence` · **Status:** Planned syllabus, not actual progress
**Weekly result:** An evaluated source-grounded QA system with cited evidence, abstention, and measurable gains versus simpler baselines.

## Daily curriculum

### Day 01 — Hybrid retrieval
- **Learn:** Sparse/dense complementarity, rank fusion, coverage.
- **Implement:** Implement RRF or justified hybrid merging plus deduplication.
- **Experiment/evaluate:** Compare BM25, dense and hybrid Recall@k/MRR with same queries.
- **Defend independently:** Why does fusion sometimes reduce quality?
- **Pass when:** Hybrid ablation and metric report.

### Day 02 — Reranking
- **Learn:** Cross-encoder scoring, precision/latency tradeoffs.
- **Implement:** Implement optional reranker on top candidates, with strict token limits.
- **Experiment/evaluate:** Measure ranking gain, p50/p95 added latency and language slices.
- **Defend independently:** What is the tradeoff between reranking depth and latency?
- **Pass when:** Fair rerank comparison recorded.

### Day 03 — Grounded answer generation
- **Learn:** Evidence context, citation IDs, temperature, abstention.
- **Implement:** Build answer generator from retrieved passages with enforced citation schema; no free-form source fabrication.
- **Experiment/evaluate:** Test answerable/unanswerable and citation resolution.
- **Defend independently:** Why are valid-looking citations not proof of correct grounding?
- **Pass when:** Cited answers trace back to real passage IDs.

### Day 04 — Answer evaluation
- **Learn:** Correctness, faithfulness, citation support, human review.
- **Implement:** Create evaluation harness for factuality/citations and abstention; annotate samples blind to variant.
- **Experiment/evaluate:** Compare baseline prompt and improved pipeline, inspect disagreement.
- **Defend independently:** How do you separate retrieval failure from generation failure?
- **Pass when:** Explicit evaluation rubric and labeled failures.

### Day 05 — Robustness
- **Learn:** Contradictory docs, irrelevant passages, multilingual queries.
- **Implement:** Run adversarial negative and conflicting-source queries; add uncertainty behavior.
- **Experiment/evaluate:** Record unsupported answers, false confidence, failure taxonomy.
- **Defend independently:** When must the system refuse or abstain?
- **Pass when:** Robustness report with examples and mitigation.

### Day 06 — Cost, context and latency
- **Learn:** Token budgets, caching, truncation, cost-quality frontier.
- **Implement:** Benchmark context sizes/rerank depth and token usage; define response contract.
- **Experiment/evaluate:** Measure latency and answer quality by settings; no guessed API cost.
- **Defend independently:** What tradeoff does a longer context window create?
- **Pass when:** Measured cost/latency-quality selection.

### Day 07 — Week 8 integration
- **Learn:** Honest claims and evaluation validity.
- **Implement:** Document architecture decisions, full retrieval→generation pipeline and retrospective.
- **Experiment/evaluate:** Reproduce evaluation and spot-check human labels.
- **Defend independently:** Defend citations, retrieval, reranking and abstention unaided.
- **Pass when:** RAG evaluation gate met or blocked with evidence.

## Weekly integration gate
- Demonstrate and reproduce: An evaluated source-grounded QA system with cited evidence, abstention, and measurable gains versus simpler baselines.
- Link actual commands, configs, runs, tests, failures and independent defense in this week's journal.
- Apply [universal quality gates](../docs/QUALITY_GATES.md), record unresolved issues, and update [sprint progress](../SPRINT_PROGRESS.md).
- Next week starts only after required evidence or explicit documented exception; do not manufacture completion.
