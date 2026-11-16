# Sprint Progress — Verified State

**Last reviewed:** 2026-11-16  
**Current sprint:** Week 01 / Day 01 — planned, not yet implemented  
**Active project:** `projects/01-classical-ml/`  
**Status:** Curriculum and governance bootstrapped; **no ML learning, experiments, model training, tests or defenses have been verified**.

## Verified repository setup
- Repository README, ignore rules, classical ML project README and Day 1 journal exist.
- [AGENTS.md](AGENTS.md) contains global mentorship, execution, security and validation rules.
- [ROADMAP.md](ROADMAP.md) indexes 12 weeks; `curriculum/week-01.md` through `week-12.md` specify all seven days each.
- [docs/QUALITY_GATES.md](docs/QUALITY_GATES.md) defines technical-evidence and security gates.
- [journal/TEMPLATE.md](journal/TEMPLATE.md) standardizes future daily records.

**These are documentation deliverables, not proof of any AI skill.**

## Active Day 1 — remaining acceptance criteria
- [ ] Acquire lawful public ULB/Kaggle fraud dataset and document exact provenance/license/hash.
- [ ] Write and run dataset inspection: schema, missing values, duplicates, counts and prevalence.
- [ ] Define leakage-aware split, baseline, metrics, and locked-final-test procedure in `projects/01-classical-ml/reports/experiment_protocol.md`.
- [ ] Commit reproducible code and observed output (never raw dataset/secrets).
- [ ] Answer the Day 1 technical-defense questions independently.
- [ ] Verify Day 1 gate against [Week 1 curriculum](curriculum/week-01.md).

## Blockers / unknowns
- Dataset not downloaded or inspected.
- Compute environment, dependency installation and Python version not yet validated.
- No experiment output or defense evidence.

## Immediate next action
Continue Week 01 Day 01. Read [Day 1 journal](journal/week-01/day-01.md), then implement the **dataset inspection and experimental design** deliverables. Do not train complex models until the protocol is justified.

## Deviations from planned curriculum
_None recorded._

## Update rules
Only mark an item verified when linked to a file, command output, benchmark, test log, screenshot where appropriate, or reviewed defense. Record failed checks and limitations. Update this file at meaningful checkpoints and do not infer progress from elapsed time.
