# RPD Theory Stack and Interfaces

## Purpose

Responsibility Pathway Design (RPD) is the design-translation layer between responsibility-pathway analysis and implementation-adjacent engineering.

It converts diagnosed pathway weaknesses into reviewable design objectives, requirements, intervention candidates, trade-off decisions, and verification obligations.

```text
Responsibility concepts
        ↓
Responsibility Pathway Model (RPM)
  analysis and diagnosis
        ↓
Responsibility Pathway Design (RPD)
  design translation and selection
        ↓
Responsibility Pathway Engineering (RPE)
  specification, implementation, checking, and operation
```

RPD is not a substitute for RPM or RPE. It defines the transformation between them.

## Core transformation

The basic RPD transformation is:

```text
RPM finding
  → design objective
  → design requirement
  → candidate interventions
  → trade-off evaluation
  → selected pathway design
  → verification obligation
  → RPE handoff
```

### Example

RPM finding:

> The actor able to detect a harmful transition cannot stop, suspend, or escalate it within the relevant time window.

Possible RPD design objectives:

- preserve timely intervention capacity;
- align detection capability with exercisable authority;
- prevent silent continuation after a high-confidence warning.

Possible requirements:

- define a suspension authority;
- define an escalation route and response deadline;
- preserve evidence at the moment of intervention;
- prevent automatic continuation while escalation is unresolved.

Possible interventions:

- direct stop authority;
- time-bounded delegated authority;
- automatic containment pending review;
- scoped rollback;
- institutional return point.

RPD does not assume one intervention is always correct. It requires alternatives and trade-offs to be visible.

## RPD analytical objects

RPD works with six primary objects.

### 1. Design objective

A desired responsibility-pathway property, such as preserved intervention capacity, contestability, evidence continuity, or residual stewardship.

### 2. Design requirement

A testable condition the pathway design must satisfy.

### 3. Intervention candidate

A possible organizational, procedural, interface, technical, contractual, or institutional change.

### 4. Trade-off record

A record of expected benefits, burdens, failure modes, power effects, and residual risks.

### 5. Selected design

The intervention set chosen for implementation, together with its rationale and rejected alternatives.

### 6. Verification obligation

The evidence needed to determine whether the selected design was implemented and whether its intended pathway property remains exercisable.

## Design dimensions

RPD does not optimize a single scalar. It treats pathway design as a multi-objective problem involving at least:

- authority–capability alignment;
- intervention timing;
- evidence continuity;
- human or institutional returnability;
- contestability;
- recovery capacity;
- affected-party accessibility;
- residual-impact stewardship;
- proportionality;
- security and privacy;
- operational burden;
- resistance to responsibility theatre and blame transfer.

Improving one dimension may weaken another. RPD therefore requires explicit trade-off reasoning rather than an unqualified claim of improvement.

## Response options

RPD distinguishes state reversal from the wider set of responsibility responses.

A pathway may preserve or lose options to:

- stop;
- suspend;
- contain;
- undo;
- correct;
- restore;
- compensate;
- explain;
- contest;
- reform;
- reopen;
- steward irreducible residue.

A technically irreversible transition is not automatically a design failure. The relevant question is whether the remaining response options are justified, accessible, resourced, and connected to responsible actors or institutions.

## Interface from RPM to RPD

An RPM finding should provide, at minimum:

- pathway and transition identifier;
- affected state change;
- relevant actors and roles;
- authority and capability mismatch, if any;
- evidence basis and uncertainty;
- lost, weakened, or inaccessible response options;
- affected parties;
- time window for intervention or recovery;
- residual impact;
- current ownership or ownership gap.

RPD should not infer certainty where RPM reports `unknown` or insufficient evidence.

## Interface from RPD to RPE

An RPD handoff should provide, at minimum:

- selected design objective;
- testable requirements;
- intervention specification;
- responsible implementation owner;
- required records and evidence;
- verification conditions;
- monitoring and review triggers;
- rollback, suspension, and reopening conditions;
- expected residual risk;
- rejected alternatives and rationale;
- privacy, security, legal, and organizational constraints.

RPE may implement and check these obligations, but implementation success does not by itself establish moral, legal, social, or affected-party acceptance.

## Boundary conditions

RPD does not claim to:

- define all meanings of responsibility;
- determine legal liability;
- certify fairness, safety, compliance, or production readiness;
- eliminate irreversible harm;
- guarantee that a formally present intervention can be exercised in practice;
- replace systems safety, human factors, requirements engineering, assurance cases, organizational governance, or incident response;
- transfer final responsibility to AI.

## Research status

RPD is a developing design framework and research program. Its vocabulary, transformation rules, patterns, evaluation protocol, and empirical support remain open to review and revision.