# RPD Assurance Interface v0.1

## Purpose

Responsibility Pathway Design (RPD) produces design objectives, testable requirements, selected interventions, trade-off records, and verification obligations. These outputs must remain traceable when they enter assurance, review, implementation, and operation.

This document defines a provisional interface between RPD and responsibility-pathway assurance activities. It does not define a certification scheme and does not treat an assurance case as proof that a pathway is safe, lawful, fair, effective, or socially accepted.

## Position in the theory stack

```text
RPM diagnosis
  → RPD design translation and selection
  → RPE specification and implementation
  → assurance argument and evidence review
  → operational monitoring and challenge
  → reopening, redesign, or continued operation
```

Assurance is not a final seal placed after implementation. It is a structured, revisable argument about whether stated responsibility-pathway claims are supported by evidence within a declared scope.

## Core distinction

RPD distinguishes five propositions that are often collapsed:

1. **Design proposition** — a selected design is expected to preserve or improve a responsibility-pathway property.
2. **Implementation proposition** — the selected design has been implemented as specified.
3. **Exercise proposition** — relevant actors can actually use the intervention under realistic conditions.
4. **Operational proposition** — the pathway continues to satisfy its requirements during operation.
5. **Broader validation proposition** — the pathway is acceptable or effective in its social, institutional, legal, and affected-party context.

Evidence for one proposition does not automatically support the others.

## Assurance package

An RPD assurance handoff should contain the following objects.

### 1. Claim set

Each claim should state:

- claim identifier;
- proposition type;
- pathway and transition scope;
- responsible claim owner;
- intended audience;
- applicable assumptions;
- exclusions and unresolved questions;
- expiry or review condition.

Claims should use bounded language such as:

- implemented according to the referenced specification;
- exercised successfully under the stated scenario;
- supported by the listed evidence within the declared scope;
- not yet validated in live operation;
- uncertain because evidence is incomplete.

### 2. Requirement trace

Every assurance claim should trace to:

```text
RPM finding
  → RPD objective
  → RPD requirement
  → selected pattern or intervention
  → RPE specification
  → implementation evidence
  → exercise or operational evidence
  → assurance claim
```

A broken trace is itself an assurance finding.

### 3. Evidence register

Each evidence item should record:

- identifier and source;
- collection method;
- date and version;
- evidence class;
- scope supported;
- limitations;
- independence or conflict-of-interest information;
- retention and access conditions;
- supersession status.

Evidence should not be silently reused outside the conditions under which it was produced.

### 4. Defeaters and counterevidence

An assurance package should identify conditions that could weaken or defeat its claims, including:

- changed assumptions;
- untested actor absence;
- timing degradation;
- unavailable authority;
- inaccessible evidence;
- organizational restructuring;
- affected-party challenge;
- conflicting legal or institutional interpretation;
- operational incidents;
- newly discovered residual impact.

Defeaters are not optional appendix material. They are part of the assurance argument.

### 5. Residual uncertainty register

Residual uncertainty should identify:

- what remains unknown;
- why it remains unknown;
- who owns the uncertainty;
- what evidence would reduce it;
- when it must be reconsidered;
- what operation is permitted while it remains unresolved.

Unknown should not be rewritten as low risk without evidence.

### 6. Review and decision record

The review record should distinguish:

- technical review;
- operational review;
- organizational review;
- affected-party or representative review;
- legal or policy review where applicable;
- final human authorization.

Review participation does not imply endorsement beyond the recorded scope.

## Assurance claim structure

A minimal claim may be represented as:

```text
Claim
  because Requirements R1..Rn are satisfied
  by Design D
  implemented through Specifications S1..Sn
  supported by Evidence E1..En
  under Assumptions A1..An
  subject to Defeaters F1..Fn
  until Review Trigger T
```

The argument should make visible where evidence is direct, inferred, simulated, exercised, or operational.

## Assurance levels

The following levels are provisional and non-certifying.

| Level | Meaning |
|---|---|
| A0 | Claim drafted; evidence not yet assembled |
| A1 | Trace and implementation evidence assembled |
| A2 | Relevant interventions exercised in defined scenarios |
| A3 | Limited operational evidence supports the claim |
| A4 | Repeated operational evidence and independent challenge available |
| A5 | Broader contextual validation has been conducted within a declared scope |

An assurance level applies to a specific claim, version, context, and time period. It must not be converted into a global score for the whole system without a separate justified method.

## Mandatory challenge questions

For each claim, reviewers should ask:

1. What exactly is being claimed?
2. Which pathway transitions are inside and outside scope?
3. Which evidence directly supports the claim?
4. Which parts depend on inference?
5. Could the responsible actor exercise the intervention under time pressure?
6. What happens if the named actor is unavailable?
7. Does the evidence show implementation, exercise, operation, or broader validation?
8. What counterevidence exists?
9. What assumptions may expire?
10. Who may challenge the claim?
11. What event forces reopening?
12. Who has authority to continue, suspend, or retire the pathway?

## Anti-theatre tests

An assurance interface should fail review when:

- a claim has no trace to an RPD requirement;
- evidence demonstrates documentation but not exercisability;
- exercise scenarios omit foreseeable actor absence or delay;
- unresolved exceptions are described as successful control operation;
- residual uncertainty has no owner;
- review triggers are absent or non-actionable;
- the same party designs, implements, verifies, and approves without disclosed independence limits;
- affected-party challenge is impossible where the design claims contestability;
- operational evidence is generalized beyond its observed context;
- assurance language implies certification or legal adequacy without authority.

## Interface with RPE

RPE should return to the assurance package:

- implementation status for each requirement;
- deviations from the selected design;
- evidence-producing mechanisms;
- exercise results;
- monitoring signals;
- incident and exception records;
- change history;
- proposed claim scope;
- known implementation limitations.

RPD retains responsibility for determining whether deviations require redesign rather than merely updated documentation.

## Reopening conditions

A claim should be reopened when any declared trigger occurs, including:

- material design or implementation change;
- failure of an intervention exercise;
- loss of authority, capability, staffing, or evidence access;
- incident affecting the claimed pathway property;
- changed affected-party impact;
- assumption expiry;
- newly identified anti-pattern;
- changed organizational or contractual boundary;
- evidence supersession;
- scheduled review date.

Reopening may lead to continued operation, constrained operation, suspension, redesign, or retirement. The assurance interface does not predetermine that decision.

## Human gate

Final acceptance, continued operation, publication, certification claims, legal conclusions, and external submission remain human decisions. An assurance package may support those decisions but cannot authorize itself.

## Research status

This interface is a developing research artifact. Its claim model, evidence structure, assurance levels, challenge process, and reopening rules remain open to critique, comparison, empirical testing, and revision.