# RPD Pattern Composition Rules v0.1

## Status

This document is a provisional research artifact for Responsibility Pathway Design (RPD). It defines how multiple pathway-design patterns may be combined, ordered, constrained, and reviewed. It does not establish safety, legality, compliance, effectiveness, or canonical theory.

## Purpose

Individual patterns are rarely sufficient for a real sociotechnical pathway. A design may require a return point, bounded delegation, interruption authority, evidence continuity, recovery ownership, and residual stewardship at the same time.

Pattern composition therefore requires more than selecting several desirable controls. It requires explicit reasoning about:

- dependency;
- ordering;
- scope;
- authority;
- timing;
- evidence;
- accessibility;
- conflict;
- operational burden;
- residual risk.

## Composition unit

A composed design should be represented as:

```text
context
  + diagnosed pathway findings
  + design objectives
  + selected pattern set
  + composition relations
  + conflict resolutions
  + verification obligations
  + residual-risk record
```

The unit of review is the composed pathway design, not the isolated pattern name.

## Composition relations

### 1. Requires

Pattern A requires Pattern B when A cannot preserve its intended pathway property without B.

Example:

- Evidence-Preserving Rollback may require Recovery Ownership.
- Contestation Hold may require a Human or Institutional Return Point.

A `requires` relation must identify:

- why the dependency exists;
- whether it is structural or context-specific;
- what fails if the dependency is absent;
- how the dependency will be verified.

### 2. Enables

Pattern A enables Pattern B when it creates a precondition that makes B exercisable.

Example:

- Scoped Approval may enable Progressive Commitment.
- Assumption Expiry may enable Reopening or Review.

An enabling relation is weaker than a required relation and should not be presented as necessary without evidence.

### 3. Constrains

Pattern A constrains Pattern B when it narrows B's scope, duration, authority, or operating conditions.

Example:

- Time-Bounded Delegation constrains Scoped Approval.
- Contestation Hold constrains automatic continuation.

Constraints should be expressed as testable bounds, not as general aspirations.

### 4. Overrides

Pattern A overrides Pattern B when a defined condition permits A to suspend or replace B temporarily.

Example:

- emergency containment may override normal Progressive Commitment;
- a legally required preservation hold may override deletion-oriented recovery procedures.

Every override relation must define:

- trigger;
- authorized actor;
- maximum scope;
- maximum duration;
- evidence requirement;
- return condition;
- review obligation.

### 5. Sequences before / after

Some patterns must occur in an order.

Example:

- Evidence preservation should precede destructive rollback;
- affected-party notice may need to precede final closure;
- recovery ownership must be assigned before incident handoff is completed.

Sequence rules must account for timing windows and cannot assume that later correction remains possible.

### 6. Runs in parallel

Patterns may operate simultaneously when responsibility pathways branch across technical, organizational, contractual, or affected-party channels.

Parallel composition requires:

- separate owners where appropriate;
- synchronization points;
- conflict escalation;
- evidence correlation;
- a clear rule for when one branch may block another.

### 7. Substitutes for

Pattern A may substitute for Pattern B only when the design records why the same objective can be met under the relevant conditions.

Substitution claims require stronger justification than simple preference. The record should identify:

- equivalent objective;
- changed assumptions;
- lost capabilities;
- new residual risks;
- verification differences.

### 8. Conflicts with

Patterns conflict when they cannot both preserve their intended properties under the same scope, timing, authority, or resource constraints.

Conflict is not automatically a defect. Unrecorded conflict is.

## Composition invariants

A composed RPD design should preserve the following provisional invariants.

### Invariant A: no orphaned objective

Every design objective must map to at least one requirement, intervention, pattern, or explicit decision not to intervene.

### Invariant B: no authority-free obligation

Every obligation must identify an actor or institution with sufficient authority and capability to perform it.

### Invariant C: no unbounded exception

Every exception, override, emergency route, or temporary delegation must have scope, duration, evidence, and return conditions.

### Invariant D: no evidence-only remedy

Recording a failure does not count as correction, restoration, compensation, contestation, or reform.

### Invariant E: no technical-only recovery claim

State rollback or system restoration must not be treated as complete responsibility recovery when affected parties, institutional obligations, compensation, explanation, or residual harm remain.

### Invariant F: no silent branch loss

When a pathway branches, each branch must have ownership, evidence, closure criteria, and residual-risk handling.

### Invariant G: no hidden conflict resolution

Trade-offs between patterns must be recorded. Selection by convenience or implementation availability alone is insufficient.

## Composition workflow

### Step 1: establish the diagnostic basis

List the RPM findings, uncertainty, affected parties, time windows, response options, and residual impact.

### Step 2: derive objectives and requirements

Translate findings into pathway properties and testable requirements before choosing patterns.

### Step 3: select candidate patterns

Identify multiple candidate pattern sets where feasible. Avoid treating the first plausible set as the design.

### Step 4: map composition relations

For each pair or group, record whether they:

- require;
- enable;
- constrain;
- override;
- sequence;
- run in parallel;
- substitute;
- conflict.

### Step 5: test invariants

Check the composed design against all composition invariants.

### Step 6: resolve conflicts

Use the conflict-resolution protocol below.

### Step 7: derive verification obligations

Separate:

- design verification;
- implementation verification;
- operational verification;
- real-world validation questions.

### Step 8: record residual risk and rejected alternatives

Do not compress unresolved uncertainty into a positive design label.

## Conflict-resolution protocol

For each conflict:

1. identify the conflicting objectives or pathway properties;
2. identify the affected actors and parties;
3. identify the timing and irreversibility constraints;
4. distinguish mandatory constraints from design preferences;
5. generate at least one alternative composition;
6. compare burden, accessibility, authority, evidence, security, privacy, recovery, and residual harm;
7. document who has authority to choose;
8. preserve dissent or unresolved uncertainty where material;
9. define monitoring and reopening conditions.

A conflict is not resolved merely because one implementation is easier.

## Common composition failures

### Pattern stacking without pathway logic

Several patterns are listed, but dependencies, conflicts, and timing are not analyzed.

### Circular authority

Two patterns each depend on approval from the actor whose conduct they are intended to constrain.

### Exception cascade

Multiple local exceptions collectively remove the pathway property the patterns were meant to preserve.

### Verification gap between patterns

Each pattern is checked individually, but no one verifies the interface between them.

### Parallel branch abandonment

One branch receives full ownership and evidence while another affected-party or organizational branch is left without closure.

### Conflict laundering

A real normative or institutional conflict is reframed as a technical configuration choice.

## RPD-to-RPE handoff for composed designs

The handoff should include:

- composition graph or relation table;
- selected pattern set;
- pattern parameters;
- sequence and concurrency rules;
- override and exception rules;
- implementation owners;
- interface obligations;
- shared evidence requirements;
- cross-pattern failure tests;
- monitoring and review triggers;
- unresolved conflicts;
- residual risks;
- rejected compositions and rationale.

RPE should be able to determine not only whether each pattern exists, but whether the composition remains exercisable as a whole.

## Research questions

- Which composition relations recur across domains?
- Which invariants are necessary, redundant, or overly broad?
- How should conflicting affected-party and institutional objectives be represented?
- What evidence distinguishes a functioning composition from responsibility theatre?
- Which composition failures are domain-specific?
- How should cross-organizational compositions be validated?

## Boundary statement

This document proposes a review structure. It does not prove that any composed design is effective in practice. Empirical cases, counterexamples, independent review, and comparison with established systems, safety, governance, requirements, and assurance methods remain necessary.