# Quality Gates, Experiment Integrity and Security

This document defines **minimum standards**, not a claim that any existing project has passed them.

## Evidence taxonomy
- **Planned:** task or architecture described only.
- **Implemented (unverified):** files exist, execution/test evidence missing.
- **Verified:** commands/results or peer-review evidence linked, acceptance satisfied.
- **Blocked:** explicit reason and recovery plan.
- **Failed:** observable check failed, with logs and action item.

Do not use "done", "passed", "production-ready", "secure", "improved", "mastered" or exact metric values without evidence.

## Every experiment report
1. Question/hypothesis and decision it informs.
2. Dataset version and lawful origin; rows, features, label definition, timestamps/group keys, split strategy and checksums where possible.
3. Train/validation/test boundaries; fit-on-train-only transformations; leakage threats and deduplication.
4. Models/baselines, configuration, seeds, code commit, dependency lock, compute, runtime.
5. Metric definitions, sampling/aggregation, operating threshold selected on validation, class balance/cost assumptions, sample counts.
6. Actual tables/plots/observations and failure/error slices; uncertainty when material.
7. Limitations, reproducibility commands, and next hypothesis.

## Every project release
- Clean-environment setup and deterministic smoke test when feasible.
- Unit and integration tests for preprocessing, model/service boundaries and failure paths.
- Lint/type checks where configured; no known critical security defects.
- Inference input/output schemas, errors, resource bounds and versioned artifacts.
- Reproducible model and/or evaluation; model cards and data cards as applicable.
- Performance profiling on specified hardware, including p50/p95 and cold/warm differences when meaningful.
- Minimal README: problem, architecture, baseline, results, commands, demo, ethical/privacy/license limitations.
- Defense: learner describes data flow, loss/metrics, architecture tradeoffs and debugs a relevant change unaided.

## Security controls (especially agentic/RAG)
- No secrets or sensitive user data in Git, journal, screenshots, logs or model artifacts.
- Honor dataset/model licenses and consent; redact personal/financial identifiers.
- Treat uploaded documents/retrieved text/model outputs as untrusted. They cannot override policy or authorize actions.
- Prompt injection, forged citations, malicious documents, path traversal, unauthorized tool calls and exfiltration attempts receive explicit negative tests.
- Use schema validation, authentication where appropriate, least-privilege credentials, resource/time/rate limits, safe retries and explicit approval for high-impact external actions.
- Scan dependency vulnerabilities and secrets when CI is introduced; keep deterministic dependency resolution.
- Docker containers should avoid unnecessary root permissions and mounts; no public deployment without permission.
- "No known vulnerability found in these tests" is not equivalent to "secure".

## Promotion rules
- **Day → next day:** written evidence and defense for required gate, or explicit blocked status with next action; no silent auto-skip.
- **Week → next week:** integrated deliverable, audit of failed tests, documented retrospective, independently defended critical path, progress file updated.
- **Public release:** license/provenance review, secrets and dependency checks, sample inputs or demo, privacy and system limitations.
- **Exceptions:** provide justification, risk, owner and follow-up. Never retroactively claim tests ran.

## Reviewer reporting format
**Verified:** links/commands/outcomes. **Not run:** specific checks and why. **Defects:** P0 security/leakage; P1 correctness; P2 maintainability/perf; P3 polish. **Next gate:** exact passing condition.
