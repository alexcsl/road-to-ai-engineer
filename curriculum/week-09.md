# Week 09 — Agent tools, security and full-stack AI integration
**Planned start:** 2027-01-11 · **Project:** `04-document-intelligence` · **Status:** Planned syllabus, not actual progress
**Weekly result:** A usable document intelligence application with controlled tools, approval boundaries, safe document ingestion and tested user workflows.

## Daily curriculum

### Day 01 — Application contracts
- **Learn:** Async jobs, API boundary design, auth/data tenancy.
- **Implement:** Define upload/query/history endpoints, response schemas, threat model; select minimal UI.
- **Experiment/evaluate:** Review PII exposure, access patterns, uploads and resource limits.
- **Defend independently:** Which operations need authorization and why?
- **Pass when:** API and threat model documented.

### Day 02 — Ingestion service
- **Learn:** Background jobs, idempotency, state transitions, retries.
- **Implement:** Implement document upload and indexing pipeline with max sizes, validation and safe paths.
- **Experiment/evaluate:** Test duplicate upload, partial parse failure, bad PDFs, timeouts.
- **Defend independently:** Why must retries be idempotent?
- **Pass when:** Stable ingestion lifecycle tests pass.

### Day 03 — AI tools & agent boundary
- **Learn:** Tool calling versus deterministic orchestration; permissions and schemas.
- **Implement:** Implement minimal read-only evidence lookup tool; optional multi-step planner only if justified.
- **Experiment/evaluate:** Test unauthorized tool calls, malformed arguments and prompt-injection instructions in documents.
- **Defend independently:** Why are retrieved documents not trusted instructions?
- **Pass when:** Tool policy tests and justification for agentic complexity.

### Day 04 — Auth & retrieval isolation
- **Learn:** Tenant isolation, identity, authorization at retrieval time.
- **Implement:** Implement safe per-user document access or single-user explicit demo with clear limitations.
- **Experiment/evaluate:** Attempt cross-user retrieval in tests if multi-user.
- **Defend independently:** How can vector similarity retrieval leak cross-tenant data?
- **Pass when:** No known unauthorized retrieval in scoped tests.

### Day 05 — Frontend integration
- **Learn:** Progress states, cited answer UI, error display.
- **Implement:** Build minimal web interface for upload, indexing status, grounded questions and citation inspection.
- **Experiment/evaluate:** Run end-to-end happy and unhappy paths, inaccessible docs and malformed uploads.
- **Defend independently:** Why must an answer show actual source offsets/pages?
- **Pass when:** Usable demo with traceable evidence.

### Day 06 — Security + resilience
- **Learn:** Rate limits, log redaction, SSRF/path injection, bounded resources.
- **Implement:** Add negative tests, request limits and safe failure behavior; lock permissions.
- **Experiment/evaluate:** Document prompt injection, exfiltration, citation forgery and denial-of-service checks.
- **Defend independently:** Describe residual security risk honestly.
- **Pass when:** Threat test results and unresolved issues documented.

### Day 07 — Week 9 review
- **Learn:** Product correctness and integration defense.
- **Implement:** Clean setup and end-to-end demo; publish deployment readiness checklist and retrospective.
- **Experiment/evaluate:** Re-run key regression/evaluation suite after integration.
- **Defend independently:** Trace one user request across frontend, retrieval, LLM and response unaided.
- **Pass when:** Flagship integrated demo and transparent evaluation.

## Weekly integration gate
- Demonstrate and reproduce: A usable document intelligence application with controlled tools, approval boundaries, safe document ingestion and tested user workflows.
- Link actual commands, configs, runs, tests, failures and independent defense in this week's journal.
- Apply [universal quality gates](../docs/QUALITY_GATES.md), record unresolved issues, and update [sprint progress](../SPRINT_PROGRESS.md).
- Next week starts only after required evidence or explicit documented exception; do not manufacture completion.
