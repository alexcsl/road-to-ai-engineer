# Week 07 — Document intelligence — parsing, corpora and retrieval
**Planned start:** 2026-12-28 · **Project:** `04-document-intelligence` · **Status:** Planned syllabus, not actual progress
**Weekly result:** A licensed multilingual document corpus and trustworthy retrieval benchmark with keyword and dense baselines.

## Daily curriculum

### Day 01 — User problem and corpus
- **Learn:** Grounded QA versus extraction, target user, citations, answerability.
- **Implement:** Select real public financial/policy docs with redistribution rights; specify business queries and corpus version.
- **Experiment/evaluate:** Audit licensing, language mix, PII, document duplicates and document-level split.
- **Defend independently:** What does the user actually gain from RAG versus search?
- **Pass when:** Corpus manifest, use cases, constraints and safety review.

### Day 02 — PDF extraction
- **Learn:** Text layouts, OCR limitations, tables, page offsets, parsing trust.
- **Implement:** Implement parse pipeline with page-level provenance, schema, error reporting and table policy.
- **Experiment/evaluate:** Compare parsed text against sampled source pages; log extraction errors.
- **Defend independently:** Why can text extraction destroy source attribution?
- **Pass when:** Deterministic parse and spot-check report.

### Day 03 — Chunking
- **Learn:** Token versus character chunking, overlap, semantic units.
- **Implement:** Implement page-aware chunking with source IDs, offsets, metadata, stable hashes.
- **Experiment/evaluate:** Compare 2–3 chunking policies for coverage/size and duplicated spans.
- **Defend independently:** How does chunk size affect retrieval precision/recall?
- **Pass when:** Reproducible chunks and provenance tests.

### Day 04 — Evaluation set
- **Learn:** Gold evidence passages, unanswerable queries, data leakage.
- **Implement:** Create balanced small human-reviewed questions with source links, bilingual cases and negative queries.
- **Experiment/evaluate:** Check no query/test answer was constructed from generated model guesses alone.
- **Defend independently:** Why is answerability annotation essential?
- **Pass when:** Versioned held-out retrieval test set with review notes.

### Day 05 — Sparse baseline
- **Learn:** BM25 lexical matching, tokenization, ranking metrics.
- **Implement:** Build BM25 index + top-k retrieval with deterministic corpus version.
- **Experiment/evaluate:** Measure Recall@k, MRR/nDCG on held-out query set.
- **Defend independently:** When does exact matching beat embeddings?
- **Pass when:** Sparse baseline metrics and examples.

### Day 06 — Dense baseline
- **Learn:** Embedding space, cosine similarity, vector indexing, multilingual capability.
- **Implement:** Build dense embedding index and retrieval with versioned model and dimensionality checks.
- **Experiment/evaluate:** Compare against BM25 on equal corpus/query set; measure latency.
- **Defend independently:** Why may semantic retrieval miss an exact identifier?
- **Pass when:** Dense baseline metrics and reproducible index.

### Day 07 — Week 7 audit
- **Learn:** Retrieval failure modes and safe provenance.
- **Implement:** Inspect hard negatives, data licensing, prompt injection in documents; retrospective.
- **Experiment/evaluate:** Re-run both indexes; analyze retrieval misses by language/query type.
- **Defend independently:** Defend chunk/index/metric selection unaided.
- **Pass when:** Retrieval benchmark and ground truth reviewed.

## Weekly integration gate
- Demonstrate and reproduce: A licensed multilingual document corpus and trustworthy retrieval benchmark with keyword and dense baselines.
- Link actual commands, configs, runs, tests, failures and independent defense in this week's journal.
- Apply [universal quality gates](../docs/QUALITY_GATES.md), record unresolved issues, and update [sprint progress](../SPRINT_PROGRESS.md).
- Next week starts only after required evidence or explicit documented exception; do not manufacture completion.
