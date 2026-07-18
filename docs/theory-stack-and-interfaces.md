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
  specification, implementation, checking, and technical operation
        ↓
Assurance
  bounded claim and evidence review
        ↓
Operational governance
  authorized continuation, constraint, suspension, redesign, or retirement
        ↓
Monitored operation and revision routes
```

RPD is not a substitute for RPM, RPE, assurance, or operational governance. It defines a transformation and handoff between them.

The detailed responsibility-transfer contract is defined in [RPD–RPE–Assurance–Operational Governance Boundary v0.1](./rpd-rpe-assurance-operational-governance-boundary-v0.1.md).

## Layer interpretation

| Layer | Primary question | Primary output |
|---|---|---|
| Responsibility concepts | what meanings and obligations of responsibility are relevant? | explicit conceptual and normative commitments |
| RPM | where is the responsibility pathway connected, weakened, or broken? | bounded diagnosis with uncertainty and affected scope |
| RPD | what pathway design should respond to the diagnosis? | objectives, requirements, alternatives, selected design, verification obligations |
| RPE | how is the selected design specified, implemented, checked, maintained, and technically operated? | implementation and deviation records, evidence and monitoring mechanisms |
| Assurance | what bounded claims are supported by what evidence and limitations? | claim package, counterevidence, defeaters, uncertainty, review state |
| Operational governance | what state is authorized under current evidence and conditions? | human- or institution-authorized state decision and follow-up obligations |
| Operation and revision | what changed in practice and where must the pathway return? | monitoring record, reopening, redesign, or re-diagnosis route |

Routine technical operation may sit with an RPE operational owner. Operational state authority does not thereby move to RPE: continuation, constraint, suspension, redesign, and retirement require an authorized human or institution.

## Core transformation

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
- performing actor or system and separate accountable implementation owner;
- required records and evidence;
- verification conditions;
- monitoring and review triggers;
- escalation destination and response deadline;
- rollback, suspension, and reopening conditions;
- expected residual risk and named residual steward;
- rejected alternatives and rationale;
- privacy, security, legal, and organizational constraints;
- prohibited substitutions and deviation-approval authority.

RPE must return a versioned deviation record when an obligation cannot be implemented as handed off. Silence or partial implementation is not acceptance.

RPE may implement and check these obligations, but implementation success does not by itself establish moral, legal, social, operational, or affected-party acceptance.

## Interface from RPE to assurance

RPE should provide:

- versioned specification and implementation records;
- evidence that implementation matches specification;
- exercise results where exercisability is claimed;
- observed-operation evidence limited to a defined period and context;
- failures, substitutions, unavailable checks, and unresolved deviations;
- evidence provenance, ownership, retention, and access conditions;
- monitoring capability and known blind spots.

Assurance reviews scoped propositions. It does not turn implementation evidence into certification or deployment permission.

## Interface from assurance to operational governance

An assurance handoff should provide:

- the exact bounded claim and claim owner;
- evidence relied upon and evidence unavailable;
- assumptions, scope limits, counterevidence, defeaters, uncertainty, and dissent;
- current assurance state;
- monitoring and reopening triggers;
- recommended state options and their conditions;
- matters outside assurance authority.

Assurance may recommend a state. Operational governance authorizes the state through a named human or institution.

## Operational governance and return routes

Operational governance owns decisions to:

- continue;
- increase monitoring;
- constrain;
- suspend;
- return for redesign;
- retire;
- reopen an assurance claim or pathway decision.

Monitoring is a shared interface:

- RPD defines pathway properties and failure conditions;
- RPE implements and maintains monitoring and evidence mechanisms;
- assurance evaluates bounded claims against the evidence;
- operational governance authorizes state changes;
- affected parties and authorized challengers provide counterevidence and contestation where applicable.

Material implementation failure returns to RPE. A failed or infeasible design returns to RPD. Incorrect pathway modelling returns to RPM. New evidence can reopen assurance and operational decisions without waiting for a scheduled review.

## Boundary conditions

RPD does not claim to:

- define all meanings of responsibility;
- determine legal liability;
- certify fairness, safety, compliance, or production readiness;
- eliminate irreversible harm;
- guarantee that a formally present intervention can be exercised in practice;
- replace systems safety, human factors, requirements engineering, assurance cases, organizational governance, or incident response;
- authorize operational state transitions;
- transfer final responsibility to AI.

No layer may silently transfer its accountability to another layer, an artifact, a framework, or an automated component.

## Research status

RPD is a developing design framework and research program. Its vocabulary, transformation rules, patterns, evaluation protocol, empirical support, assurance boundary, and operational-governance interface remain open to review and revision.