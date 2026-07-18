# RPD–RPE–Assurance–Operational Governance Boundary v0.1

## Status

Developing interface specification for review. This document clarifies responsibility transfer across design, engineering, assurance, and operational governance. It does not certify a system, authorize deployment, determine legal liability, or transfer final responsibility to AI.

## Purpose

The responsibility pathway must remain traceable after RPD produces a selected design. This interface separates four functions that are often collapsed:

1. design translation and selection;
2. specification, implementation, and technical maintenance;
3. bounded assurance review;
4. authorized operational state decisions.

Routine technical operation may be performed by an RPE implementation or operational owner, but decisions to continue, constrain, suspend, redesign, or retire remain with an authorized human or institution.

## Lifecycle

```text
RPM diagnosis
  → RPD design translation
  → RPE specification and implementation
  → assurance review
  → operational governance decision
  → monitored operation
  → challenge, incident, or changed assumption
  → assurance reopening and/or RPD redesign
  → RPM re-diagnosis when the pathway model itself is no longer adequate
```

## Responsibility boundary

| Layer | Primary accountable role | Required outputs | May do | Must not claim or authorize |
|---|---|---|---|---|
| RPD | named human or institutional design authority | design objective, testable requirements, intervention selection, trade-off record, verification obligations, reopening conditions | translate findings into reviewable pathway designs | implementation completion, certification, deployment authorization, legal or social adequacy |
| RPE | named implementation owner and named operational owner | specification, implementation record, deviations, evidence mechanisms, monitoring capability, maintenance and rollback procedures | implement, test, maintain, operate technical and procedural mechanisms within authority | redefine RPD requirements unilaterally, certify broader adequacy, authorize contested operational states without delegated authority |
| Assurance | named claim owner and reviewers with declared independence | bounded claims, evidence trace, assumptions, counterevidence, defeaters, uncertainty, review state, recommendation | assess whether stated evidence supports a scoped proposition | convert a bounded argument into certification, erase uncertainty, substitute for legal, affected-party, or operational authority |
| Operational governance | authorized human or institution | state decision, rationale, conditions, duration, escalation, evidence-preservation instruction, redesign or retirement order | continue, watch, constrain, suspend, redesign, retire, or reopen | delegate final accountability to the framework, an automated component, or an assurance artifact |

## RPD → RPE handoff contract

An RPD handoff is complete only when it identifies:

- pathway, transition, finding, and requirement identifiers;
- selected design and rejected alternatives;
- performing actor or system and separate accountable owner;
- acceptance criteria and prohibited substitutions;
- required records and evidence mechanisms;
- verification conditions for design, implementation, exercise, operation, and broader validation where applicable;
- assumptions, constraints, residual risks, and known unknowns;
- stop, suspension, rollback, compensation, reopening, and residual-stewardship conditions;
- monitoring signals, response deadlines, escalation destination, and evidence-preservation duties;
- the authority that may approve deviations.

RPE must return an explicit deviation record when an obligation cannot be implemented as handed off. Silence, partial implementation, or documentation-only substitution does not count as acceptance.

## RPE → Assurance handoff contract

RPE must provide evidence sufficient to distinguish at least:

- specification exists;
- implementation matches the specification;
- the mechanism can be exercised under stated scenarios;
- operation has been observed during a defined period and context;
- limitations, failures, substitutions, and unavailable evidence;
- unresolved deviations from RPD requirements;
- provenance, version, access, retention, and ownership of evidence.

A successful implementation check does not establish operational effectiveness, affected-party accessibility, legal adequacy, social acceptance, fairness, safety, or whole-system readiness.

## Assurance → Operational Governance handoff contract

The assurance handoff must state:

- the exact claim under review;
- claim owner and review owner;
- evidence relied upon and evidence not available;
- assumptions and scope limits;
- counterevidence, defeaters, uncertainty, and dissent;
- current assurance state;
- monitoring and reopening triggers;
- recommended state options and their conditions;
- matters that remain outside assurance authority.

Assurance may recommend but does not itself authorize continuation, restriction, suspension, redesign, or retirement unless a separate and explicit institutional delegation exists.

## Operational state authority

Operational governance owns state-transition decisions. Minimum states are:

- **Stable** — bounded continuation under current conditions;
- **Watch** — continuation with increased monitoring;
- **Review** — evidence or assumptions require formal reconsideration;
- **Constrained** — operation continues only within narrowed conditions;
- **Suspended** — relevant operation is paused pending decision;
- **Redesign** — existing pathway design is inadequate and returns to RPD;
- **Retired** — the pathway or intervention is withdrawn from authorized use.

Every transition must record the authorized decision-maker, evidence basis, effective time, duration or review date, affected scope, residual-impact owner, and required follow-up.

## Monitoring responsibility

Monitoring is a shared interface, not a transfer of authority.

- RPD defines which pathway properties and failure conditions matter.
- RPE implements and maintains monitoring and evidence mechanisms.
- Assurance evaluates whether monitoring evidence supports bounded claims.
- Operational governance decides what state change follows a signal.
- Affected parties and authorized challengers must have a route to introduce counterevidence or contest a state.

An automated monitor may generate a signal or execute a pre-authorized containment action. It must not silently convert that signal into a final governance decision.

## Return and reopening routes

| Observed condition | Primary return route |
|---|---|
| implementation does not match specification | RPE correction; assurance claim remains limited or suspended |
| requirement is infeasible, contradictory, or produces unacceptable burden | RPD redesign |
| monitoring mechanism is absent or unreliable | RPE remediation and assurance reopening |
| evidence defeats or materially narrows a claim | assurance reopening; operational review |
| operational state becomes unsafe, inaccessible, unchallengeable, or unsupported | operational constraint or suspension; RPD redesign |
| actors, authority, transitions, or affected scope were modelled incorrectly | RPM re-diagnosis followed by RPD revision |
| irreversible residue remains after all feasible response options | named residual-stewardship route; not closure by omission |

## Deviation control

A deviation is material when it changes authority, timing, accessibility, evidence continuity, contestability, recovery, residual stewardship, burden distribution, or a verification obligation.

Material deviations require:

1. a versioned deviation record;
2. named implementation and design owners;
3. impact and residual-risk analysis;
4. assurance review of affected claims;
5. operational authorization before use, where operation is affected;
6. return to RPD when the selected design is no longer preserved.

## Non-transfer principles

- Evidence production does not transfer accountability to the evidence system.
- Assurance review does not transfer accountability to the reviewer or framework.
- Technical operation does not transfer state authority to the operator unless explicitly delegated.
- Human authorization does not erase engineering, assurance, or institutional duties.
- A formally named owner without capability, resources, access, or authority is not an adequate responsibility pathway.

## Boundary tests

The interface fails review when any of the following is true:

- RPE can silently reinterpret a requirement;
- assurance language is treated as certification or deployment permission;
- operational state changes have no named human or institutional authority;
- monitoring signals lack response deadlines or escalation destinations;
- deviations, counterevidence, or failed checks disappear from the record;
- redesign is replaced by documentation repair despite a material pathway failure;
- routine operation leaves residual impacts without a steward;
- an automated component becomes the final accountable actor.

## Research boundary

This specification is a developing research interface. It defines traceability and authority expectations, not a universal organizational structure. Sector-specific law, regulation, safety engineering, security, human factors, labor arrangements, and affected-party governance remain necessary where applicable.