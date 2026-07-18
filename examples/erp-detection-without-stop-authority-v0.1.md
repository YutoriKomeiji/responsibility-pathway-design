# Worked RPD Transformation: Detection Without Stop Authority

## Status

Illustrative worked example. It is not a finding about a specific organization and does not establish safety, compliance, legal liability, or operational adequacy.

## 1. Scenario

A production ERP pricing change is deployed after technical testing and approval. A business operations analyst can detect abnormal downstream pricing within minutes, but the analyst cannot suspend the change, halt affected transactions, or trigger an automatic containment mechanism.

The formal escalation route reaches the change owner and business approver, but expected response time is longer than the period in which incorrect transactions may accumulate.

## 2. RPM-style finding input

- Pathway: pricing-rule change from approval through production operation and recovery
- Relevant transition: production execution -> anomaly detection -> intervention
- Affected state change: incorrect prices may be committed to downstream transactions
- Detection capability: business operations analyst
- Stop or suspension authority: change manager or designated technical owner
- Intervention window: shorter than normal escalation response time
- Evidence basis: monitoring alert, transaction sample, approval record, authorization matrix
- Uncertainty: alert may be false or locally scoped
- Affected parties: customers, sales operations, finance, downstream processors
- Weakened response options: stop, contain, timely correct
- Residual impact: correction work, customer communication, financial reconciliation, trust impact

## 3. Classification

Primary:

- F1 Authority-capability mismatch

Secondary:

- F3 Scope discontinuity, if monitoring scope differs from the actual affected scope
- F6 Recovery ownership failure, if technical rollback has no corresponding business-recovery owner

## 4. Design objectives

### O1. Preserve timely containment

A credible detector must be able to initiate containment within the harm-development window.

### O2. Preserve evidence at intervention

The system must retain the alert, observed transactions, active version, decision record, and intervention action.

### O3. Avoid uncontrolled authority expansion

The design must not grant broad, permanent production authority merely because one role can detect anomalies.

### O4. Connect technical rollback to business recovery

Restoring a prior configuration must not be treated as complete recovery when incorrect transactions remain.

## 5. Requirements

### R1. Bounded suspension initiation

> When a defined high-severity pricing anomaly trigger occurs, an authorized operations analyst shall be able to initiate a scoped suspension within five minutes, preserve the active configuration and affected-transaction evidence, and invoke the emergency change owner if suspension cannot be confirmed.

### R2. Automatic expiration

> A suspension initiated under R1 shall expire or require reauthorization after a defined interval unless a designated authority extends, replaces, or closes it.

### R3. Evidence preservation

> The intervention process shall retain the trigger, initiator, scope, timestamp, system version, affected objects, approvals, overrides, and subsequent recovery decisions.

### R4. Business-recovery ownership

> When incorrect transactions have been committed, a named business recovery owner shall coordinate correction, notification, reconciliation, compensation where applicable, and residual-impact tracking.

### R5. Reopening condition

> Nominal closure shall be reopenable when additional affected transactions, unresolved customer impact, or contradictory evidence is identified.

## 6. Candidate interventions

### C1. Direct permanent stop authority

Grant the analyst standing authority to stop the full pricing process.

Benefits:

- fastest intervention;
- simple operational path.

Burdens and risks:

- excessive authority concentration;
- higher false-stop impact;
- weak proportionality for uncertain or local anomalies.

### C2. Time-bounded scoped suspension

Allow trained analysts to suspend only the affected pricing condition, region, channel, or transaction class for a limited time.

Benefits:

- aligns intervention with detection;
- limits blast radius;
- preserves time for review.

Burdens and risks:

- requires reliable scoping;
- may miss broader effects;
- interface and authorization complexity.

### C3. Automatic containment pending review

Automatically isolate or pause affected transactions when a validated high-severity trigger fires.

Benefits:

- consistent and fast;
- less dependent on availability of one role.

Burdens and risks:

- false positives may interrupt business;
- trigger quality becomes critical;
- automation can obscure who owns continuation.

### C4. Accelerated escalation only

Retain current authority structure but create an emergency response route.

Benefits:

- minimal authority redesign;
- lower implementation burden.

Burdens and risks:

- still dependent on responder availability;
- may remain slower than the harm-development window;
- can become nominal escalation without real intervention.

## 7. Trade-off decision

Provisional selection:

- C2 time-bounded scoped suspension;
- C4 emergency escalation as fallback;
- technical support from C3 only after trigger validation;
- R4 business-recovery ownership independent of technical rollback.

Rationale:

C2 preserves timely intervention while avoiding unrestricted standing authority. C4 remains necessary when scope is unclear or suspension fails. Automatic containment may be introduced for narrowly validated triggers, but it should not replace accountable continuation and recovery decisions.

Rejected as sole design:

- C1, because permanent full-stop authority is disproportionate to the uncertainty and role scope;
- C4 alone, because escalation without timely intervention does not resolve the original pathway weakness;
- C3 alone, because automation cannot own continuation, remedy, or residual impact.

## 8. Verification obligations

### Design verification

Confirm that the design specifies:

- authorized initiators;
- scope limits;
- trigger criteria;
- time limit;
- evidence capture;
- fallback escalation;
- continuation authority;
- business-recovery ownership;
- reopening conditions.

### Implementation verification

Test that:

- the analyst can initiate a scoped suspension;
- unauthorized scope expansion is blocked;
- evidence is retained;
- suspension expires or is reauthorized;
- escalation is delivered and acknowledged;
- affected transactions can be identified.

### Operational validation

Run exercises including:

- a true high-severity anomaly;
- a false positive;
- an ambiguous-scope event;
- an unavailable change owner;
- a failed suspension command;
- a case where technical rollback succeeds but customer and financial recovery remains incomplete.

## 9. Anti-theatre review

The pathway remains defective if:

- the analyst sees a suspend button but lacks real permission;
- suspension requires approval that exceeds the harm window;
- logs exist but no one owns correction;
- the incident is closed after rollback despite unresolved downstream impact;
- the analyst becomes the blame target without receiving authority, support, or protection;
- affected customers cannot obtain explanation or correction.

## 10. RPE handoff boundary

RPE may specify and check permissions, state transitions, evidence fields, expiry behavior, escalation records, and reopening conditions.

RPE implementation cannot by itself establish that five minutes is legally, ethically, or operationally sufficient; that the selected scope is fair; or that affected parties recognize the recovery as adequate. Those judgments require domain evidence and human review.