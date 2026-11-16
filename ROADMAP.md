# Road to AI Engineer — 12-week authoritative curriculum index

**Start:** Monday 2026-11-16 (Asia/Jakarta). **Planned Week 12 ends:** Sunday 2027-02-07. **Target:** 35–45 focused hours/week, adjustable; these dates do **not** certify completion. Career: AI Engineer first, Full-Stack Engineer second.

## Read order for agents
1. [AGENTS.md](AGENTS.md) — global mentoring, engineering, safety and progress rules.
2. [SPRINT_PROGRESS.md](SPRINT_PROGRESS.md) — what is actually verified now.
3. This roadmap — curriculum scope and dependencies.
4. [Week-specific daily specification](curriculum/week-01.md) — exact teaching, build, experiments, defense, and day gates.
5. [Quality gates](docs/QUALITY_GATES.md) and active journal/project files.

**Do not improvise a new curriculum when these documents answer the question.** Future-week files are **planned requirements only**. Do not pre-create fake execution records or mark future tasks complete.

## Overall schedule and projects

| Week | Dates (Mon–Sun) | Technical focus | Required deliverable | Full details |
|---|---|---|---|---|
| 01 | Nov 16–22 | Fraud ML: data, leakage, baselines, eval | Reproducible fraud classification experiment, final test report | [Week 01](curriculum/week-01.md) |
| 02 | Nov 23–29 | Fraud ML: API, validation, operationalization | Tested inference API, packaging, Docker demo and case study | [Week 02](curriculum/week-02.md) |
| 03 | Nov 30–Dec 06 | PyTorch, tensor operations, CNN fundamentals | Custom training loop and CNN baseline | [Week 03](curriculum/week-03.md) |
| 04 | Dec 07–13 | CV transfer learning, robust evaluation, serving | Compared vision models and inference demo | [Week 04](curriculum/week-04.md) |
| 05 | Dec 14–20 | NLP data, tokenization, transformers, baseline | Multilingual NLP evaluation baseline and dataset protocol | [Week 05](curriculum/week-05.md) |
| 06 | Dec 21–27 | LLM fine-tuning, PEFT, evaluation and serving | Fine-tuned model, model card, reproducible comparison | [Week 06](curriculum/week-06.md) |
| 07 | Dec 28–Jan 03 | Document ingestion and retrieval | Dataset, chunking + retrieval benchmark | [Week 07](curriculum/week-07.md) |
| 08 | Jan 04–10 | RAG/reranking/grounded evaluation | Measured RAG pipeline vs retrieval baselines | [Week 08](curriculum/week-08.md) |
| 09 | Jan 11–17 | Controlled tools, UX, security | End-to-end multilingual document AI demo | [Week 09](curriculum/week-09.md) |
| 10 | Jan 18–24 | MLOps, versioning, pipelines and CI | Reproducible builds, registry, quality gates | [Week 10](curriculum/week-10.md) |
| 11 | Jan 25–31 | Inference optimization and operations | Performance and reliability benchmarks | [Week 11](curriculum/week-11.md) |
| 12 | Feb 01–07 | Technical portfolio + external validation | Public evidence package, reviews and applications | [Week 12](curriculum/week-12.md) |

**Project locations:** `projects/01-classical-ml/` (W01–02); `projects/02-deep-learning-cv/` (W03–04); `projects/03-nlp-llm/` (W05–06); `projects/04-document-intelligence/` (W07–11). W12 consolidates. New folders are created when activated, not to simulate progress.

## Weekly execution contract
Each week has seven numbered days, each with five parts: **Learn / Build / Experiment-Evaluate / Defend / Pass when**. Follow them in order unless the learner's verified evidence justifies faster advancement. Day 7 is a weekly audit, not a day for falsifying missing outputs. The learner must answer defense items before receiving a model answer, and at least one critical path per week should be implemented or modified without AI-generated code.

Required day gate: (a) deliverables exist, (b) relevant tests/experiments actually executed or blocker logged, (c) decisions/metrics documented, (d) learner independently demonstrates conceptual understanding. A failing gate stays open. At week end update `SPRINT_PROGRESS.md`, journal retrospective and project README with verified state.

## Common model/evaluation principles
- Split and freeze data before model selection; avoid source, entity, near-duplicate and time leakage; preprocessing must fit only allowed data.
- Record baseline, primary and secondary task metrics, test isolation, configs/seeds, compute environment, failures, and limitations.
- Train/fine-tune at feasible scale; no GPU requirement to claim learning. CPU/small-model fallback is valid if objectives are met and tradeoffs stated.
- Use **one final test evaluation** after freezing decisions; do not quietly tune on the held-out test.
- For latency and memory comparisons, specify machine, batch size, precision, concurrency and warmup.
- For public demos, handle credentials, abuse, document injection, access control, licensing and data privacy.
- Refer to [QUALITY_GATES](docs/QUALITY_GATES.md) before claiming project completeness.

## Exceptions, pacing and real progress
The roadmap is intentionally ambitious. If compute, work or university constraints intervene, retain core learning and evidence gates but adjust timeboxes; do not mark an unfinished week complete. Any scope/sequence change must be logged in `SPRINT_PROGRESS.md` under "deviations", with why, who approved and what validation remains.

**Current verified execution status always lives in `SPRINT_PROGRESS.md`**, not this planned syllabus.
