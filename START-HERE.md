# Start Here — Responsibility Pathway Design (RPD)

RPD is a developing design framework for translating responsibility-pathway weaknesses and admitted normative inputs into reviewable design requirements, intervention alternatives, trade-off decisions, and verification obligations.

## One-sentence orientation

> Responsibility Pathway Design asks not only **who is responsible**, but how responsibility remains connected across judgment, delegation, execution, interruption, contestation, recovery, and residual impact.

## Where RPD sits

```text
RPM — analyze and diagnose responsibility pathways
  ↓
RPD — translate findings and admitted normative inputs into designs
  ↓
RPE — specify, implement, check, maintain, and technically operate
  ↓
Assurance — review bounded claims and evidence
  ↓
Operational governance — authorize state decisions and reopening
```

RPD is not another prompt, context, harness, or local execution technique. It works at the sociotechnical design layer across people, organizations, interfaces, procedures, evidence, and technical systems.

## Read according to your goal

### Understand the framework

1. [`docs/theory-stack-and-interfaces.md`](./docs/theory-stack-and-interfaces.md)
2. [`docs/transformation-kernel-v0.1.md`](./docs/transformation-kernel-v0.1.md)
3. [`docs/verification-validation-vocabulary-v0.1.md`](./docs/verification-validation-vocabulary-v0.1.md)
4. [`docs/principles.md`](./docs/principles.md)
5. [`docs/layer-model.md`](./docs/layer-model.md)

### Apply it to a review

1. [`docs/normative-source-input-contract-v0.1.md`](./docs/normative-source-input-contract-v0.1.md)
2. [`docs/operating-questions.md`](./docs/operating-questions.md)
3. [`docs/failure-and-repair-examples.md`](./docs/failure-and-repair-examples.md)
4. [`templates/rpd-transformation-record-v0.1.md`](./templates/rpd-transformation-record-v0.1.md)
5. [`templates/rpd-verification-validation-record-v0.1.md`](./templates/rpd-verification-validation-record-v0.1.md)

### Compare it with nearby work

1. [`docs/terminology-and-nearby-concepts.md`](./docs/terminology-and-nearby-concepts.md)
2. [`docs/positioning-above-harness-engineering.md`](./docs/positioning-above-harness-engineering.md)

### Test, challenge, and revise the framework

1. [`docs/empirical-validation-protocol-v0.1.md`](./docs/empirical-validation-protocol-v0.1.md)
2. [`docs/falsification-and-theory-revision-v0.1.md`](./docs/falsification-and-theory-revision-v0.1.md)
3. [`docs/worked-case-package-guide-v0.1.md`](./docs/worked-case-package-guide-v0.1.md)
4. [`docs/case-corpus-protocol-v0.1.md`](./docs/case-corpus-protocol-v0.1.md)
5. [`docs/coding-and-adjudication-manual-v0.1.md`](./docs/coding-and-adjudication-manual-v0.1.md)

### Audit cross-document consistency

1. [`docs/cross-document-integration-audit-v0.1.md`](./docs/cross-document-integration-audit-v0.1.md)
2. Use its traceability, responsibility-boundary, terminology, template-coverage, and navigation matrices.

## Verification and validation vocabulary

Use the proposition level that matches the evidence object:

- **D — design verification:** the design artifact contains the required relationships and constraints;
- **I — implementation verification:** the approved design was implemented as specified;
- **X — exercise verification:** relevant actors can exercise it in defined scenarios;
- **O — operational verification:** observed live operation supports the bounded claim;
- **V — broader contextual validation:** wider institutional, legal, social, organizational, or affected-party evidence addresses the validation question.

Do not infer the next level from the previous one. `Operational validation` is deprecated for new artifacts because it may ambiguously mean X, O, or V.

## Minimal RPD workflow

```text
1. Receive an RPM finding and/or an authorized normative-source input.
2. Preserve source, scope, interpretation, uncertainty, and approval status.
3. Identify the responsibility-pathway property that should be preserved.
4. Write one or more testable design requirements.
5. Generate organizational, procedural, interface, technical, or institutional alternatives.
6. Compare benefits, burdens, power effects, failure modes, and residual risks.
7. Select a design and record rejected alternatives.
8. Define D/I/X/O/V obligations and bounded evidence requirements.
9. Hand the design to RPE or another implementation process.
10. Feed exercise, operational, contextual, and challenge evidence back into assurance, analysis, and redesign.
```

## A small example

**Finding:** A frontline operator can detect a harmful transition but cannot stop or escalate it before the intervention window expires.

**Possible objective:** Preserve timely intervention capacity and align detection capability with exercisable authority.

**Candidate interventions:**

- direct suspension authority;
- time-bounded delegated authority;
- automatic containment pending review;
- expedited institutional return point.

**Verification obligations:**

- D: authority, triggers, timing, evidence, and fallback are specified;
- I: the control and evidence mechanism conform to the approved design;
- X: authorized actors exercise the control under realistic scenarios;
- O: live evidence supports or does not support the bounded operational claim;
- V: broader outcome and affected-party questions remain separately evaluated.

RPD does not prescribe one universal answer. It makes alternatives and trade-offs inspectable.

## Important distinctions

- A named owner is not necessarily a continuous responsibility pathway.
- A log is not completed responsibility.
- A human-in-the-loop is not meaningful when the human lacks time, information, authority, or practical ability to intervene.
- Technical rollback is not automatically business, social, legal, or relational recovery.
- Irreversibility is not automatically a defect; it must be justified, proportionate, and accompanied by appropriate remaining response options.
- A documented control is not sufficient when it cannot be exercised in practice.
- D does not establish I; I does not establish X; X does not establish O; O does not establish V.

## Current status

> [!CAUTION]
> RPD remains under active development and has not been externally validated, standardized, certified, or approved for legal, safety, compliance, fairness, or production-readiness determinations.

The public repository exists so that the vocabulary, examples, assumptions, and design logic can be inspected and criticized. Strong counterexamples and negative results are part of the research program, not exceptions to it.
