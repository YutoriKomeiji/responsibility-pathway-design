# Responsibility Pathway Design (RPD)

> **Designing how responsibility remains connected across judgment, delegation, execution, interruption, recovery, and residual impact in AI-involved sociotechnical systems.**

[Start here](./START-HERE.md) · [Theory stack](./docs/theory-stack-and-interfaces.md) · [Transformation kernel](./docs/transformation-kernel-v0.1.md) · [Pattern language](./docs/pattern-language-v0.1.md) · [Operating questions](./docs/operating-questions.md)

---

## The problem

AI systems increasingly participate in judgment and execution. Naming an owner, preserving a log, or adding a human-in-the-loop can still leave a responsibility pathway broken.

RPD asks:

- where responsibility-bearing transitions occur;
- where authority, capability, evidence, or intervention become disconnected;
- how responsibility returns to a human or institution;
- who can stop, contest, repair, compensate, reopen, or steward residual impact;
- how a diagnosed pathway weakness should be translated into a reviewable design.

## The core idea

```mermaid
flowchart LR
    A[Responsibility concepts] --> B[RPM: analyze and diagnose]
    B --> C[RPD: translate and select designs]
    C --> D[RPE: specify, implement, check, operate]
    D --> E[Operational evidence and revision]
    E --> B
```

RPD is the design-translation layer between:

- **Responsibility Pathway Model (RPM)** — analysis and diagnosis;
- **Responsibility Pathway Engineering (RPE)** — specification, implementation, checking, and operation.

RPD converts findings into:

```text
finding
  → design objective
  → testable requirement
  → intervention alternatives
  → trade-off record
  → selected design
  → verification obligation
```

## What RPD designs

RPD treats pathway design as a multi-objective problem. Relevant dimensions include:

| Dimension | Design question |
|---|---|
| Authority–capability alignment | Can the actor who detects a problem actually intervene? |
| Intervention timing | Can intervention occur before the relevant option expires? |
| Evidence continuity | Can decisions, assumptions, and changes be reconstructed? |
| Returnability | Is there an accountable human or institutional return point? |
| Contestability | Can affected parties understand and challenge the transition? |
| Recovery capacity | Are correction, restoration, compensation, and reform resourced? |
| Residual stewardship | Who remains responsible for what cannot be undone? |
| Proportionality | Is irreversibility justified by the purpose and stakes? |
| Anti-theatre | Are controls exercisable, or merely documented? |

RPD does **not** assume that every transition should be reversible. It distinguishes state reversal from the wider set of response options: stop, suspend, contain, undo, correct, restore, compensate, explain, contest, reform, reopen, and steward irreducible residue.

## Reading paths

### First visit

1. [Start Here](./START-HERE.md)
2. [Theory Stack and Interfaces](./docs/theory-stack-and-interfaces.md)
3. [Transformation Kernel v0.1](./docs/transformation-kernel-v0.1.md)
4. [Principles](./docs/principles.md)
5. [Layer Model](./docs/layer-model.md)

### Practice and review

- [Pattern Language v0.1](./docs/pattern-language-v0.1.md)
- [Anti-Patterns v0.1](./docs/anti-patterns-v0.1.md)
- [Transformation Record Template](./templates/rpd-transformation-record-v0.1.md)
- [Worked ERP Transformation Example](./examples/erp-detection-without-stop-authority-v0.1.md)
- [Failure and Repair Examples](./docs/failure-and-repair-examples.md)
- [Operating Questions](./docs/operating-questions.md)
- [Positioning above Harness Engineering](./docs/positioning-above-harness-engineering.md)
- [Terminology and Nearby Concepts](./docs/terminology-and-nearby-concepts.md)

## Intended uses

RPD may support:

- AI deployment and workflow design reviews;
- pre-mortem and post-incident analysis;
- organizational redesign around AI-involved execution;
- responsibility handoff and escalation design;
- review of interruption, rollback, remedy, and residual ownership;
- research on responsibility-pathway design patterns and evaluation.

## Research status and boundaries

> [!IMPORTANT]
> RPD is a developing design framework and research program. It is not an established academic discipline, legal doctrine, certification framework, or proof of safety, fairness, compliance, or production readiness.

RPD does not:

- transfer final responsibility to AI;
- determine legal liability;
- replace systems safety, human factors, requirements engineering, assurance cases, incident response, or institutional governance;
- treat logging as completed responsibility;
- treat technical rollback as completed recovery;
- guarantee that a formally documented intervention can be exercised in practice.

This public repository is a reviewable design surface. Canonical publication decisions, external submissions, legal conclusions, and final human judgments remain subject to explicit human approval.

## Background

RPD developed from a Japanese essay series on responsibility pathways and from ongoing work on RPM and RPE. Those writings document the conceptual genealogy, but they are not substitutes for scholarly evidence or external validation.

- [Author page on note](https://note.com/dantarg)

## Contributing and critique

Critical comparison, counterexamples, terminology corrections, pattern proposals, and failure cases are welcome. Strong contributions should distinguish:

- observed evidence from interpretation;
- descriptive pathway mapping from normative judgment;
- structural verification from real-world validation;
- technical rollback from responsibility recovery.
