---
layout: default
title: Responsibility Pathway Design
---

# Responsibility Pathway Design (RPD)

> **Designing how responsibility remains connected across judgment, delegation, execution, interruption, recovery, and residual impact in AI-involved sociotechnical systems.**

[Start here](./START-HERE.html) · [Theory stack](./docs/theory-stack-and-interfaces.html) · [Transformation kernel](./docs/transformation-kernel-v0.1.html) · [Pattern language](./docs/pattern-language-v0.1.html) · [Evaluation protocol](./docs/evaluation-protocol-v0.1.html) · [GitHub repository](https://github.com/YutoriKomeiji/responsibility-pathway-design)

---

## Why RPD exists

AI systems increasingly participate in judgment and execution. Yet naming an owner, preserving a log, or inserting a nominal human review does not guarantee that responsibility remains connected.

RPD asks:

- Where do responsibility-bearing transitions occur?
- Where do authority, capability, evidence, or intervention become disconnected?
- Who can stop, contest, repair, compensate, reopen, or steward residual impact?
- How should a diagnosed pathway weakness become a reviewable design?

## Theory stack

```text
Responsibility concepts
        ↓
RPM — analyze and diagnose
        ↓
RPD — translate findings and select designs
        ↓
RPE — specify, implement, check, and operate
        ↓
Operational evidence, assurance, and revision
```

RPD is the design-translation layer between responsibility-pathway diagnosis and implementation-adjacent engineering.

## Core transformation

```text
RPM finding
  → design objective
  → testable requirement
  → intervention alternatives
  → trade-off record
  → selected design
  → verification obligation
  → RPE handoff
```

## Current method surface

### 1. Transformation kernel

The transformation kernel defines provisional finding classes and a disciplined route from diagnosis to design requirements, interventions, trade-offs, verification obligations, and implementation handoff.

[Read the transformation kernel](./docs/transformation-kernel-v0.1.html)

### 2. Pattern language

The pattern language provides reusable responsibility-pathway interventions, including return points, scoped approval, time-bounded delegation, progressive commitment, contestation holds, evidence-preserving rollback, recovery ownership, residual stewardship, assumption expiry, and cross-organization handoff contracts.

[Read the pattern language](./docs/pattern-language-v0.1.html)

### 3. Anti-pattern catalog

The anti-pattern catalog identifies recurring structures such as nominal human review, approval without intervention power, logging without remedy, rollback treated as recovery, orphaned residual harm, and documentation-only responsibility.

[Read the anti-pattern catalog](./docs/anti-patterns-v0.1.html)

### 4. Composition and evaluation

RPD defines relations among patterns, provisional composition invariants, conflict-resolution rules, evidence classes, layered verification and validation, and a reusable composition-evaluation record.

- [Pattern composition rules](./docs/pattern-composition-rules-v0.1.html)
- [Evaluation protocol](./docs/evaluation-protocol-v0.1.html)
- [Composition and evaluation record](./templates/rpd-composition-evaluation-record-v0.1.html)

## Design dimensions

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
| Anti-theatre | Are controls exercisable rather than merely documented? |

## Reading paths

### First visit

1. [Start Here](./START-HERE.html)
2. [Theory Stack and Interfaces](./docs/theory-stack-and-interfaces.html)
3. [Principles](./docs/principles.html)
4. [Layer Model](./docs/layer-model.html)

### Method and application

1. [Transformation Kernel](./docs/transformation-kernel-v0.1.html)
2. [Pattern Language](./docs/pattern-language-v0.1.html)
3. [Anti-Patterns](./docs/anti-patterns-v0.1.html)
4. [Pattern Composition Rules](./docs/pattern-composition-rules-v0.1.html)
5. [Evaluation Protocol](./docs/evaluation-protocol-v0.1.html)
6. [Worked ERP Example](./examples/erp-detection-without-stop-authority-v0.1.html)

### Assurance, operation, and empirical revision

1. [Assurance Interface](./docs/assurance-interface-v0.1.html)
2. [Operational Monitoring and Reopening](./docs/operational-monitoring-and-reopening-v0.1.html)
3. [Empirical Validation Protocol](./docs/empirical-validation-protocol-v0.1.html)
4. [Falsification and Theory Revision](./docs/falsification-and-theory-revision-v0.1.html)
5. [Worked Case Package Guide](./docs/worked-case-package-guide-v0.1.html)
6. [AI-Assisted Benefit Review Worked Case](./examples/ai-assisted-benefit-review-worked-case-v0.1.html)
7. [Case Corpus Protocol](./docs/case-corpus-protocol-v0.1.html)
8. [Coding and Adjudication Manual](./docs/coding-and-adjudication-manual-v0.1.html)
9. [Case Corpus Manifest](./templates/rpd-case-corpus-manifest-v0.1.html)
10. [Cross-Document Integration Audit](./docs/cross-document-integration-audit-v0.1.html)

## Research status and boundaries

> **RPD is a developing design framework and research program.** It is not an established academic discipline, legal doctrine, certification method, or proof of safety, fairness, compliance, effectiveness, social acceptance, or production readiness.

RPD does not transfer final responsibility to AI, determine legal liability, replace systems safety or human factors, or treat logging and technical rollback as completed responsibility recovery.

Canonical publication decisions, external submissions, legal conclusions, and final human judgments remain subject to explicit human approval.

---

[Explore the repository](https://github.com/YutoriKomeiji/responsibility-pathway-design) · [Author background](https://note.com/dantarg)
