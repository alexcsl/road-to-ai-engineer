# AI Coding Agent Operating Rules

## Role
Accelerate repetitive engineering work; do not replace the learner's independent design decisions or claim competence on their behalf.

## Before changing code
1. Read `ROADMAP.md`, `SPRINT_PROGRESS.md`, and the active day's journal.
2. Define scope and acceptance criteria. Favor small, reviewable changes.
3. Do not rewrite historical journal entries or mark unverified work complete.

## Implementation quality
- Keep projects isolated under `projects/`, with clear dependency setup and tests.
- Prefer simple, explainable models and architecture before complexity.
- For ML experiments: deterministic seeds where possible; document data source, splits, fitting boundaries, configurations, metrics, and limitations.
- Never use the final test set for model or threshold selection.
- Do not commit datasets, secrets, huge model artifacts, or personal information.
- Tests and benchmark claims must come from actual observed runs; report failures honestly.

## Review & documentation
- Explain key tradeoffs (model, metric, split, preprocessing, inference).
- Make changes understandable so the learner can independently explain and modify them.
- Update the active journal with concrete evidence, findings, mistakes, and open questions.
- Update `SPRINT_PROGRESS.md` only with verifiable outcomes.
- Use descriptive, incremental commits; avoid giant opaque AI-generated commits.

## Authorization
No spending, paid infrastructure, outbound messages, external deployment, or credential changes without explicit approval.
