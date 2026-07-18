# Responsibility Pathway Design Anti-Patterns v0.1

## Status

Research draft. These anti-patterns identify recurring structures that can make a responsibility pathway appear governed while leaving intervention, repair, contestation, or residual ownership weak.

They are diagnostic prompts, not findings about any specific system. Their presence should be established with evidence and context.

## How to use this document

For each suspected anti-pattern:

1. identify the pathway and transition;
2. distinguish observed evidence from interpretation;
3. record who has authority, capability, evidence, and time to act;
4. identify lost or inaccessible response options;
5. transform the finding through the RPD kernel;
6. compare alternative interventions and residual risks.

---

## Anti-pattern 1: Nominal Human-in-the-Loop

### Surface appearance

A human is present in the workflow, so the system is described as human-controlled.

### Structural defect

The human lacks sufficient time, information, competence, independence, or practical authority to change the outcome.

### Warning signs

- review time is shorter than the time needed to understand the case;
- automation output is accepted by default;
- rejection requires disproportionate justification;
- the reviewer cannot access relevant evidence;
- override is technically possible but institutionally discouraged;
- performance targets punish intervention.

### Design response direction

Align review scope, evidence access, timing, authority, and incentives. Consider Scoped Approval, Contestation Hold, Progressive Commitment, or a Human or Institutional Return Point.

---

## Anti-pattern 2: Approval Without Intervention Power

### Surface appearance

A named approver signs off on a decision or system state.

### Structural defect

The approver cannot stop, suspend, modify, escalate, or require remediation after approval conditions fail.

### Warning signs

- approval is recorded but not connected to execution controls;
- changed conditions do not invalidate approval;
- the approver cannot see downstream use;
- responsibility remains with the approver while control moves elsewhere.

### Design response direction

Bind approval to scope, expiry, material-change rules, and exercisable intervention rights.

---

## Anti-pattern 3: Logging Without Remedy

### Surface appearance

The pathway is considered accountable because events, decisions, or model outputs are logged.

### Structural defect

No actor is obligated and resourced to interpret the record, intervene, repair harm, compensate affected parties, or revise the system.

### Warning signs

- logs have no review owner;
- alerts do not change pathway state;
- evidence is inaccessible to affected parties or investigators;
- retention is emphasized while remedy is undefined;
- incident closure depends on record completion rather than recovery.

### Design response direction

Connect evidence continuity to return points, Recovery Ownership, Contestation Hold, and reopening conditions.

---

## Anti-pattern 4: Rollback Equals Recovery

### Surface appearance

A previous technical state is restored, so the incident is considered resolved.

### Structural defect

Rollback does not address already-produced decisions, disclosures, financial effects, reputational harm, affected-party needs, or institutional causes.

### Warning signs

- incident closure occurs immediately after restoration;
- no inventory of downstream effects exists;
- evidence is destroyed during rollback;
- compensation, explanation, correction, and reform are absent;
- residual harm has no owner.

### Design response direction

Use Evidence-Preserving Rollback together with Recovery Ownership and Residual Stewardship.

---

## Anti-pattern 5: Orphaned Residual Harm

### Surface appearance

The immediate incident response is complete.

### Structural defect

Long-lived, irreversible, uncertain, or distributed effects remain without a steward, monitoring duty, resource commitment, or reopening route.

### Warning signs

- responsibility ends when the project or vendor contract ends;
- no successor is named after organizational change;
- affected parties have no continuing contact route;
- uncertainty is recorded but not monitored;
- residual effects are treated as outside scope.

### Design response direction

Create Residual Stewardship with succession, monitoring, disclosure, support, and reopening rules.

---

## Anti-pattern 6: Downstream Blame Sink

### Surface appearance

A downstream operator, vendor, reviewer, or end user is named as responsible for a failed outcome.

### Structural defect

The downstream actor receives responsibility without the authority, evidence, resources, or design influence needed to prevent or repair the failure.

### Warning signs

- upstream assumptions and constraints are hidden;
- handoff acceptance is inferred from delivery;
- weaker parties carry broad indemnity or review duties;
- upstream actors retain control but disclaim consequences;
- escalation routes terminate at the least powerful actor.

### Design response direction

Use a Cross-Organization Handoff Contract, authority-capability alignment, shared evidence duties, and explicit residual ownership.

---

## Anti-pattern 7: Permanent Temporary Delegation

### Surface appearance

Exceptional or temporary authority is justified by urgency, staffing, experimentation, or transition.

### Structural defect

The delegation has no effective expiry, automatic return, independent renewal review, or evidence that the original condition continues.

### Warning signs

- renewal is automatic;
- the temporary state lasts longer than the stated trigger;
- no actor owns authority reclamation;
- expiry produces a notice but no state change;
- delegated powers expand through operational habit.

### Design response direction

Use Time-Bounded Delegation and Assumption Expiry, with automatic reversion or safe suspension.

---

## Anti-pattern 8: Unreviewable Closure

### Surface appearance

A pathway or incident is marked closed.

### Structural defect

Closure lacks preserved evidence, acceptance criteria, affected-party input, residual-risk ownership, or conditions under which the matter can be reopened.

### Warning signs

- closure authority is unclear;
- unresolved objections disappear from the active record;
- evidence is deleted or fragmented;
- closure means monitoring stops;
- no reopening trigger or route exists.

### Design response direction

Define closure as a governed transition with evidence preservation, explicit residual risk, review authority, and reopening conditions.

---

## Anti-pattern 9: Evidence Scope Inflation

### Surface appearance

A test result, audit, formal model, benchmark, approval, certification, or successful execution is treated as evidence for a broader claim.

### Structural defect

The claimed conclusion exceeds the tested object, assumptions, environment, time period, population, or verification method.

### Warning signs

- technical verification is presented as real-world validation;
- one environment is generalized to all deployments;
- a current result is treated as permanent;
- the evidence owner and validity conditions are missing;
- downstream summaries omit scope limitations.

### Design response direction

Use Scoped Approval, Assumption Expiry, explicit claim-to-evidence links, and separate verification from validation.

---

## Anti-pattern 10: Automatic Continuation After Exception

### Surface appearance

An exception is recorded, escalated, or queued for review.

### Structural defect

The pathway continues before the exception is resolved, making the human or institutional review practically irrelevant.

### Warning signs

- escalation does not alter system state;
- review deadlines exceed the action window;
- warnings are advisory only for high-impact transitions;
- missing evidence defaults to continuation;
- unresolved challenges are reviewed retrospectively only.

### Design response direction

Use Contestation Hold, Progressive Commitment, a return point, and explicit hold/release authority.

---

## Anti-pattern 11: Responsibility by Documentation

### Surface appearance

Roles, policies, controls, or escalation paths are documented, so responsibility is considered adequately designed.

### Structural defect

The documented pathway is not exercisable under real staffing, incentives, access constraints, emergencies, or organizational power relations.

### Warning signs

- procedures are never rehearsed;
- named owners are unaware of the role;
- emergency access is unavailable;
- no budget or staffing supports the duty;
- actual practice relies on informal workarounds.

### Design response direction

Add operational validation, exercises, resource checks, and evidence that authority can be exercised within the relevant time window.

---

## Anti-pattern 12: Single-Owner Compression

### Surface appearance

One person or team is named as the owner of the entire pathway.

### Structural defect

Distinct duties for decision, execution, evidence, challenge, recovery, and residual stewardship are compressed into a label that obscures capability gaps or conflicts of interest.

### Warning signs

- the owner cannot perform all required response modes;
- oversight and execution are held by the same role without safeguards;
- absence of the owner breaks the pathway;
- ownership language substitutes for transition-level design;
- affected parties cannot identify the appropriate route for a specific need.

### Design response direction

Decompose ownership by transition and response mode while preserving an accountable coordination point.

## Relationship to patterns

Anti-pattern detection does not mechanically determine a single remedy. The same defect may require different interventions depending on stakes, timing, affected parties, organizational structure, and residual risk.

A credible RPD record should state:

- which anti-pattern is suspected;
- what evidence supports that interpretation;
- where the pattern label does not fully fit;
- which response options are lost or weakened;
- which intervention alternatives were considered;
- why the selected design is proportionate;
- what verification and validation remain necessary.

Anti-pattern labels must not be used as substitutes for evidence, legal conclusions, intent claims, or blame assignment.