---
layout: default
title: Responsibility Pathway Design
---

# Responsibility Pathway Design (RPD)

> **Designing how responsibility remains connected across judgment, delegation, execution, interruption, recovery, and residual impact in AI-involved sociotechnical systems.**

**Current status:** **provisional, reviewable RPD v0.1 research baseline**. This indicates internal coherence and inspectability only; it does not establish external validation, certification, legal authority, safety, compliance, production readiness, or authorization to operate.

[Start here](./START-HERE.html) · [Theory stack](./docs/theory-stack-and-interfaces.html) · [Transformation kernel](./docs/transformation-kernel-v0.1.html) · [Normative-source contract](./docs/normative-source-input-contract-v0.1.html) · [Verification vocabulary](./docs/verification-validation-vocabulary-v0.1.html) · [Stabilization audit](./docs/rpd-v0.1-stabilization-and-release-readiness-audit.html) · [Pattern language](./docs/pattern-language-v0.1.html) · [Boundary interface](./docs/rpd-rpe-assurance-operational-governance-boundary-v0.1.html) · [日本語README](https://github.com/YutoriKomeiji/responsibility-pathway-design/blob/main/README.ja.md) · [GitHub repository](https://github.com/YutoriKomeiji/responsibility-pathway-design)

---

## Why RPD exists

AI systems increasingly participate in judgment and execution. Yet naming an owner, preserving a log, or inserting a nominal human review does not guarantee that responsibility remains connected.

RPD asks:

- Where do responsibility-bearing transitions occur?
- Where do authority, capability, evidence, or intervention become disconnected?
- Who can stop, contest, repair, compensate, reopen, or steward residual impact?
- How should a diagnosed pathway weakness or authorized normative constraint become a reviewable design?

## Theory stack

```text
Responsibility concepts and authorized normative sources
        ↓
RPM — analyze and diagnose
        ↓
RPD — translate inputs and select designs
        ↓
RPE — specify, implement, check, and technically operate
        ↓
Assurance — review bounded claims and evidence
        ↓
Operational governance — authorize state decisions
        ↓
Operational evidence, challenge, reopening, and revision
```

RPD is the design-translation layer between responsibility-pathway diagnosis, authorized normative inputs, and implementation-adjacent engineering.

## Core transformation

```text
RPM finding and/or admitted normative-source input
  → design objective
  → testable requirement
  → intervention alternatives
  → trade-off record
  → selected design
  → D/I/X/O/V verification and validation obligations
  → RPE handoff
```

## Verification and validation vocabulary

| Code | Proposition |
|---|---|
| D | Design verification |
| I | Implementation verification |
| X | Exercise verification |
| O | Operational verification |
| V | Broader contextual validation |

Evidence at one level does not automatically support the next. `Operational validation` is deprecated for new artifacts because it can ambiguously refer to X, O, or V.

- [Read the vocabulary](./docs/verification-validation-vocabulary-v0.1.html)
- [Use the record template](./templates/rpd-verification-validation-record-v0.1.html)

## Current method surface

### 1. Transformation kernel and normative inputs

The transformation kernel defines provisional finding classes and a disciplined route from diagnosis or admitted normative input to design requirements, interventions, trade-offs, verification obligations, and implementation handoff.

- [Transformation kernel](./docs/transformation-kernel-v0.1.html)
- [Normative-source input contract](./docs/normative-source-input-contract-v0.1.html)

### 2. Pattern language

The pattern language provides reusable responsibility-pathway interventions, including return points, scoped approval, time-bounded delegation, progressive commitment, contestation holds, evidence-preserving rollback, recovery ownership, residual stewardship, assumption expiry, and cross-organization handoff contracts.

[Read the pattern language](./docs/pattern-language-v0.1.html)

### 3. Anti-pattern catalog

The anti-pattern catalog identifies recurring structures such as nominal human review, approval without intervention power, logging without remedy, rollback treated as recovery, orphaned residual harm, and documentation-only responsibility.

[Read the anti-pattern catalog](./docs/anti-patterns-v0.1.html)

### 4. Composition, evaluation, and assurance

RPD defines relations among patterns, provisional composition invariants, conflict-resolution rules, evidence classes, bounded D/I/X/O/V propositions, assurance claims, and operational-governance boundaries.

- [Pattern composition rules](./docs/pattern-composition-rules-v0.1.html)
- [Evaluation protocol](./docs/evaluation-protocol-v0.1.html)
- [Verification vocabulary](./docs/verification-validation-vocabulary-v0.1.html)
- [Composition and evaluation record](./templates/rpd-composition-evaluation-record-v0.1.html)
- [Verification and validation record](./templates/rpd-verification-validation-record-v0.1.html)
- [Assurance interface](./docs/assurance-interface-v0.1.html)
- [RPD–RPE–Assurance–Operational Governance boundary](./docs/rpd-rpe-assurance-operational-governance-boundary-v0.1.html)

### 5. Stabilization and review readiness

The stabilization audit records the bounded meaning of the provisional RPD v0.1 baseline, current traceability coverage, authority boundaries, navigation coverage, unresolved work, and conditions that should reopen the baseline.

- [RPD v0.1 stabilization and release-readiness audit](./docs/rpd-v0.1-stabilization-and-release-readiness-audit.html)
- [Cross-document integration audit](./docs/cross-document-integration-audit-v0.1.html)

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
3. [Transformation Kernel](./docs/transformation-kernel-v0.1.html)
4. [Normative-Source Input Contract](./docs/normative-source-input-contract-v0.1.html)
5. [Verification and Validation Vocabulary](./docs/verification-validation-vocabulary-v0.1.html)
6. [RPD v0.1 Stabilization Audit](./docs/rpd-v0.1-stabilization-and-release-readiness-audit.html)

### Method and application

1. [Pattern Language](./docs/pattern-language-v0.1.html)
2. [Anti-Patterns](./docs/anti-patterns-v0.1.html)
3. [Pattern Composition Rules](./docs/pattern-composition-rules-v0.1.html)
4. [Evaluation Protocol](./docs/evaluation-protocol-v0.1.html)
5. [Verification and Validation Record](./templates/rpd-verification-validation-record-v0.1.html)
6. [Worked ERP Example](./examples/erp-detection-without-stop-authority-v0.1.html)

### Assurance, operation, and empirical revision

1. [Boundary Interface](./docs/rpd-rpe-assurance-operational-governance-boundary-v0.1.html)
2. [Assurance Interface](./docs/assurance-interface-v0.1.html)
3. [Operational Monitoring and Reopening](./docs/operational-monitoring-and-reopening-v0.1.html)
4. [Empirical Validation Protocol](./docs/empirical-validation-protocol-v0.1.html)
5. [Falsification and Theory Revision](./docs/falsification-and-theory-revision-v0.1.html)
6. [Worked Case Package Guide](./docs/worked-case-package-guide-v0.1.html)
7. [AI-Assisted Benefit Review Worked Case](./examples/ai-assisted-benefit-review-worked-case-v0.1.html)
8. [Case Corpus Protocol](./docs/case-corpus-protocol-v0.1.html)
9. [Coding and Adjudication Manual](./docs/coding-and-adjudication-manual-v0.1.html)
10. [Case Corpus Manifest](./templates/rpd-case-corpus-manifest-v0.1.html)
11. [Cross-Document Integration Audit](./docs/cross-document-integration-audit-v0.1.html)

## Research status and boundaries

> **RPD is a developing design framework and research program.** It is not an established academic discipline, legal doctrine, certification method, or proof of safety, fairness, compliance, effectiveness, social acceptance, or production readiness.

Following approval of the stabilization audit, RPD v0.1 may be described as a **provisional, reviewable research baseline**. This describes internal coherence and inspectability only. External review, empirical validation, comparative evaluation, standardization, certification, and operational authorization remain open.

RPD does not transfer final responsibility to AI, determine legal liability, invent or finally interpret normative sources, replace systems safety or human factors, or treat logging and technical rollback as completed responsibility recovery.

Canonical publication decisions, external submissions, legal conclusions, release tags, and final human judgments remain subject to explicit human approval.

---

[Explore the repository](https://github.com/YutoriKomeiji/responsibility-pathway-design) · [日本語README](https://github.com/YutoriKomeiji/responsibility-pathway-design/blob/main/README.ja.md) · [Author background](https://note.com/dantarg)