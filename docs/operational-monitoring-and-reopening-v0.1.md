# Operational Monitoring and Reopening Protocol v0.1

## Purpose

A responsibility-pathway design can degrade after approval even when its implementation remains unchanged. Authority may move, staff may leave, evidence systems may fail, response times may lengthen, affected-party impact may change, or temporary delegation may become permanent.

This protocol defines how RPD assurance claims should remain connected to operation, challenge, and redesign.

## Monitoring object

Monitoring should observe responsibility-pathway properties rather than only system uptime or model performance.

Relevant properties include:

- authority–capability alignment;
- intervention timing;
- evidence continuity;
- returnability;
- contestability;
- recovery capacity;
- residual stewardship;
- assumption validity;
- cross-organizational handoff integrity;
- accessibility of intervention and remedy.

## Signal classes

### M1 — Structural signals

Examples:

- role or organizational change;
- modified approval authority;
- changed delegation boundary;
- supplier or contract change;
- modified workflow or interface;
- changed data-retention policy.

### M2 — Exercise signals

Examples:

- failed or delayed stop exercise;
- escalation route not reachable;
- rollback performed without recovery ownership;
- actor unable to locate required evidence;
- contestation channel unavailable.

### M3 — Operational signals

Examples:

- intervention deadline missed;
- unresolved exceptions accumulating;
- repeated manual bypass;
- growing residual-impact backlog;
- stale assumptions;
- unexplained ownership transfer.

### M4 — Incident and challenge signals

Examples:

- harm or near miss;
- affected-party challenge;
- whistleblowing or internal dissent;
- conflicting evidence;
- external audit finding;
- legal, policy, or institutional change.

### M5 — Absence signals

The absence of expected evidence is itself a signal, including:

- no completed exercises;
- no review records;
- no response to challenge;
- no named residual owner;
- no evidence of remedy completion;
- no confirmation that temporary delegation ended.

## Trigger model

Each assurance claim should define:

- monitored signals;
- source and collection interval;
- warning threshold;
- reopening threshold;
- immediate suspension condition;
- responsible monitor;
- escalation destination;
- maximum response time;
- required evidence preservation.

Thresholds should be justified by pathway stakes and option expiry, not chosen only for operational convenience.

## Reopening states

| State | Meaning |
|---|---|
| Stable | Current evidence remains within declared claim conditions |
| Watch | Warning signal detected; increased observation required |
| Review | Claim scope or assumptions require formal reconsideration |
| Constrained | Continued operation allowed only under stated limits |
| Suspended | Relevant transition or pathway paused pending decision |
| Redesign | RPD requirements or selected composition must change |
| Retired | The pathway or claim is no longer authorized for use |

A transition between states should record the decision owner, rationale, evidence, duration, and exit criteria.

## Reopening procedure

1. Preserve the triggering evidence.
2. Identify the affected claim, requirement, pattern, and transition.
3. Determine whether the signal concerns implementation, exercise, operation, or broader validation.
4. Check whether a declared defeater has occurred.
5. Identify response options that remain available.
6. Assign uncertainty and residual-impact owners.
7. Decide the temporary operating state.
8. Re-run relevant tests and challenge questions.
9. Determine whether documentation repair is sufficient or RPD redesign is required.
10. Record the human decision and next review trigger.

## Redesign boundary

The following conditions normally require return to RPD rather than assurance-document revision alone:

- the design objective no longer addresses the observed pathway weakness;
- requirements cannot be exercised under realistic conditions;
- pattern composition creates an unresolved conflict;
- authority and capability have become structurally separated;
- contestability or remedy depends on an inaccessible actor;
- residual impact has no viable steward;
- an assumption essential to selection is no longer defensible;
- the selected design produces a new material pathway break.

## Monitoring anti-patterns

### Dashboard without authority

Signals are visible, but no actor can intervene within the relevant window.

### Threshold without rationale

A metric threshold exists, but its connection to pathway stakes or option expiry is unexplained.

### Alert closure without repair

An alert is marked resolved when the notification was acknowledged, not when the pathway weakness was repaired.

### Permanent watch state

A claim remains indefinitely under watch without escalation, redesign, or explicit risk acceptance.

### Exercise substitution

Scheduled exercises are treated as sufficient operational evidence even when operating conditions differ materially.

### Silent scope reduction

A failing claim is preserved by narrowing its scope without recording who approved the reduction or what remains uncovered.

### Missing absence detection

Monitoring checks positive events but cannot detect that expected evidence, review, or intervention never occurred.

## Minimum operational record

For each reporting period, record:

- claim and pathway version;
- observed signals;
- missed or unavailable signals;
- exercises completed and failed;
- incidents, challenges, and exceptions;
- assumption changes;
- residual-impact status;
- state transitions;
- reopened claims;
- redesign requests;
- human decisions;
- next review date.

## Boundaries

Monitoring cannot establish that unobserved harms did not occur. A stable dashboard does not prove a sound responsibility pathway. This protocol does not replace incident response, safety monitoring, legal review, affected-party engagement, or independent assurance.