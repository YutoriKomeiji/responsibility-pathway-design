---
layout: default
title: Responsibility Pathway Design
---

# Responsibility Pathway Design (RPD)

> **Design where responsibility should stop, return, transfer, recover, and remain visible when AI participates in real work.**

RPD is a public design framework for AI-involved sociotechnical systems. It helps teams find where responsibility, authority, evidence, intervention, recovery, or residual ownership can break — and turn those findings into reviewable design requirements.

[Start here](./START-HERE.html) · [Pattern language](./docs/pattern-language-v0.1.html) · [Worked ERP example](./examples/erp-detection-without-stop-authority-v0.1.html) · [Transformation kernel](./docs/transformation-kernel-v0.1.html) · [Verification vocabulary](./docs/verification-validation-vocabulary-v0.1.html) · [日本語README](https://github.com/YutoriKomeiji/responsibility-pathway-design/blob/main/README.ja.md) · [GitHub repository](https://github.com/YutoriKomeiji/responsibility-pathway-design)

---

## Where RPD helps

RPD is useful when “add a human approval step” is not enough.

Typical design questions include:

- Can the person or system that detects a problem actually stop or change the process?
- Does responsibility remain connected when work moves between humans, AI agents, SaaS, and existing systems?
- Can evidence survive delegation, automation, retry, repair, and restart?
- Who owns effects that cannot be fully reversed?
- Can affected parties challenge a decision or trigger reopening?
- How should a diagnosed weakness or an authorized policy requirement become a testable design obligation?

Common use cases include AI deployment review, workflow redesign, pre-mortem analysis, post-incident analysis, escalation design, repair/recovery design, and responsibility-handoff design.

## What RPD produces

```text
input basis
  → design objective
  → testable requirement
  → intervention alternatives
  → trade-off record
  → selected design
  → verification obligation
  → assurance and reopening conditions
```

RPD does not assume that every risky pathway should simply be closed. It distinguishes among stopping, constraining, suspending, containing, correcting, restoring, compensating, contesting, reopening, and stewarding residual impact.

## How it fits with the other Responsibility Pathway projects

```text
RPM — analyze and diagnose responsibility-pathway weaknesses
  ↓
RPD — translate findings and admitted requirements into designs
  ↓
RPE — specify, implement, and check technical responsibility controls
  ↓
Assurance — review bounded claims and evidence
  ↓
Operational governance — authorize real continuation, suspension, or reopening
```

RPD is the design-translation layer. It does not replace implementation, assurance, or operational authority.

## Start with a concrete case

If this is your first visit, use this order:

1. [Start Here](./START-HERE.html)
2. [Worked ERP Example](./examples/erp-detection-without-stop-authority-v0.1.html)
3. [Pattern Language](./docs/pattern-language-v0.1.html)
4. [Transformation Kernel](./docs/transformation-kernel-v0.1.html)
5. [Verification and Validation Vocabulary](./docs/verification-validation-vocabulary-v0.1.html)

The worked case is a faster entry point than reading the full theory stack first.

## Core design dimensions

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

## Normative-source inputs

RPD can receive human- or institution-approved inputs derived from laws, public guidance, standards, organizational policies, professional duties, and affected-party commitments.

RPD does not automatically interpret or create those requirements. Source authority, scope, interpretation, uncertainty, conflict, approval, expiry, review ownership, and reopening conditions should be established before normative input enters design work.

## Verification levels

RPD separates five evidence levels:

| Code | Evidence object |
|---|---|
| D | Design verification |
| I | Implementation verification |
| X | Exercise verification |
| O | Operational verification |
| V | Broader contextual validation |

Evidence at one level does not automatically establish the next.

[Read the verification vocabulary](./docs/verification-validation-vocabulary-v0.1.html)

## Current maturity and public use

RPD v0.1 is a **provisional, reviewable research baseline**.

That means the framework is still open to external review, empirical testing, comparison, revision, and counterexamples. It does **not** mean readers should avoid applying or critiquing it.

Real design use is valuable because it can reveal:

- patterns that are too expensive to operate;
- Human Gates that become rubber-stamping;
- controls that shift risk to affected parties;
- pathways that fail under time pressure;
- actions that are technically reversible but socially irreversible;
- simpler alternatives that work better.

See the repository's [public review and use posture](https://github.com/YutoriKomeiji/responsibility-pathway-design/blob/main/PUBLIC_REVIEW_AND_USE.md).

## Important boundaries

RPD does not by itself:

- transfer final responsibility to AI;
- determine legal liability;
- create or finally interpret law, policy, ethics, standards, or affected-party mandates;
- replace systems safety, human factors, requirements engineering, assurance, incident response, or institutional governance;
- treat logging as completed responsibility;
- treat technical rollback as completed recovery;
- turn an assurance record into certification or operational authorization.

These are responsibility boundaries. They are different from research claims that may improve through evidence and review.

## Explore the method

### Design method

- [Pattern Language](./docs/pattern-language-v0.1.html)
- [Anti-Patterns](./docs/anti-patterns-v0.1.html)
- [Pattern Composition Rules](./docs/pattern-composition-rules-v0.1.html)
- [Evaluation Protocol](./docs/evaluation-protocol-v0.1.html)
- [Transformation Record Template](./templates/rpd-transformation-record-v0.1.html)

### Assurance and operation

- [RPD–RPE–Assurance–Operational Governance Boundary](./docs/rpd-rpe-assurance-operational-governance-boundary-v0.1.html)
- [Assurance Interface](./docs/assurance-interface-v0.1.html)
- [Operational Monitoring and Reopening](./docs/operational-monitoring-and-reopening-v0.1.html)

### Empirical revision

- [Empirical Validation Protocol](./docs/empirical-validation-protocol-v0.1.html)
- [Falsification and Theory Revision](./docs/falsification-and-theory-revision-v0.1.html)
- [Empirical Research Roadmap](./docs/empirical-research-roadmap-v0.1.html)

---

RPD uses CC BY 4.0 for documentation/design/research material and MIT for software or executable scripts explicitly identified as software. See [LICENSING.md](https://github.com/YutoriKomeiji/responsibility-pathway-design/blob/main/LICENSING.md).
