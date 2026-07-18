# Start Here — Responsibility Pathway Design (RPD)

RPD is a developing design framework for translating responsibility-pathway weaknesses into reviewable design requirements, intervention alternatives, trade-off decisions, and verification obligations.

## One-sentence orientation

> Responsibility Pathway Design asks not only **who is responsible**, but how responsibility remains connected across judgment, delegation, execution, interruption, contestation, recovery, and residual impact.

## Where RPD sits

```text
RPM — analyze and diagnose responsibility pathways
  ↓
RPD — translate findings into design objectives and interventions
  ↓
RPE — specify, implement, check, and operate the selected design
```

RPD is not another prompt, context, harness, or local execution technique. It works at the sociotechnical design layer across people, organizations, interfaces, procedures, evidence, and technical systems.

## Read according to your goal

### Understand the framework

1. [`docs/theory-stack-and-interfaces.md`](./docs/theory-stack-and-interfaces.md)
2. [`docs/principles.md`](./docs/principles.md)
3. [`docs/layer-model.md`](./docs/layer-model.md)

### Apply it to a review

1. [`docs/operating-questions.md`](./docs/operating-questions.md)
2. [`docs/failure-and-repair-examples.md`](./docs/failure-and-repair-examples.md)
3. Record the finding, affected transition, lost response options, design objective, alternatives, and verification obligation.

### Compare it with nearby work

1. [`docs/terminology-and-nearby-concepts.md`](./docs/terminology-and-nearby-concepts.md)
2. [`docs/positioning-above-harness-engineering.md`](./docs/positioning-above-harness-engineering.md)

## Minimal RPD workflow

```text
1. Receive an RPM finding or equivalent pathway diagnosis.
2. Identify the responsibility-pathway property that should be preserved.
3. Write one or more testable design requirements.
4. Generate organizational, procedural, interface, technical, or institutional alternatives.
5. Compare benefits, burdens, power effects, failure modes, and residual risks.
6. Select a design and record rejected alternatives.
7. Define the evidence needed to verify implementation and continued exercisability.
8. Hand the design to RPE or another implementation process.
9. Feed operational evidence back into analysis and redesign.
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

- authority is documented;
- the control is technically and procedurally exercisable;
- response deadlines are monitored;
- evidence is preserved at intervention;
- unresolved escalation prevents silent automatic continuation.

RPD does not prescribe one universal answer. It makes alternatives and trade-offs inspectable.

## Important distinctions

- A named owner is not necessarily a continuous responsibility pathway.
- A log is not completed responsibility.
- A human-in-the-loop is not meaningful when the human lacks time, information, authority, or practical ability to intervene.
- Technical rollback is not automatically business, social, legal, or relational recovery.
- Irreversibility is not automatically a defect; it must be justified, proportionate, and accompanied by appropriate remaining response options.
- A documented control is not sufficient when it cannot be exercised in practice.

## Current status

> [!CAUTION]
> RPD remains under active development and has not been externally validated, standardized, certified, or approved for legal, safety, compliance, fairness, or production-readiness determinations.

The public repository exists so that the vocabulary, examples, assumptions, and design logic can be inspected and criticized. Strong counterexamples and negative results are part of the research program, not exceptions to it.
