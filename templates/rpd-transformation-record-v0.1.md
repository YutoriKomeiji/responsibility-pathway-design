# RPD Transformation Record v0.1

## Reader and AI-use contract

This is a **reviewable design record**, not an authorization decision. Human readers should be able to trace each chosen intervention to an input and a verification obligation. AI-assisted editors must preserve the distinctions among *observed fact*, *inference*, *design proposal*, and *approved decision*.

- Preserve source IDs, verbatim uncertainties, rejected alternatives, dissent, and the original evidence level.
- Leave a field as `unknown` or `not evaluated` when the evidence does not support it; never fabricate an owner, policy approval, exercise, metric, or result.
- A machine-generated draft is `draft` until a named eligible authority reviews it. An AI-generated route or completed template does **not** grant Authority.
- Before handoff, check that every requirement links to a source, owner, verification obligation, and reopening trigger.
- For nontrivial handoffs, use Section 8A to identify eligible receivers and the allowable next action. Do not default to Human Return merely because a route is blocked.

## Record control

- Transformation ID:
- Version:
- Date:
- Author / review team:
- Status: draft / reviewed / approved / implemented / retired
- Source RPM finding IDs:
- Normative-source input IDs:
- Target RPE handoff ID:

## 1. Input basis

Classify each objective and mandatory constraint as `RPM-derived`, `normative-source-derived`, `combined`, `design assumption`, or `human judgment`.

### RPM finding and pathway context

- Pathway:
- Transition(s):
- Affected state change:
- Relevant actors and institutions:
- Affected parties:

### Evidence and uncertainty

- Evidence basis:
- Confidence:
- Unknowns:
- Competing interpretations:

### Normative-source record

Complete one row per source. Use the [Normative-Source Input Contract v0.1](../docs/normative-source-input-contract-v0.1.md).

| Source ID | Type | Issuing authority | Citation / version | Scope | Binding status | Interpreted obligation | Interpretation owner | Uncertainty / dissent | Approval status | Review trigger |
|---|---|---|---|---|---|---|---|---|---|---|
| N-1 |  |  |  |  |  |  |  |  |  |  |

### Normative-source conflicts

- Conflicting or overlapping sources:
- Applicable priority rule, if authorized:
- Affected-party burdens under competing interpretations:
- Interim containment or suspension condition:
- Named decision authority:
- Decision, rationale, and dissent:
- Reopening trigger:

### Response-option condition

Mark each as available, weakened, unavailable, unknown, or not applicable.

| Response option | Status | Evidence / explanation |
|---|---|---|
| Stop |  |  |
| Suspend |  |  |
| Contain |  |  |
| Undo |  |  |
| Correct |  |  |
| Restore |  |  |
| Compensate |  |  |
| Explain |  |  |
| Contest |  |  |
| Reform |  |  |
| Reopen |  |  |
| Steward residue |  |  |

## 2. Finding classification

- [ ] F1 Authority-capability mismatch
- [ ] F2 Evidence discontinuity
- [ ] F3 Scope discontinuity
- [ ] F4 Return-point failure
- [ ] F5 Contestation failure
- [ ] F6 Recovery ownership failure
- [ ] F7 Assumption expiry failure
- [ ] F8 Cross-boundary handoff failure
- [ ] Other / proposed extension:
- [ ] No RPM finding; normative-source-only input

Rationale:

## 3. Design objectives

For each objective, state the pathway property rather than a preferred mechanism.

| ID | Design objective | Input basis | Source IDs | Priority | Affected parties | Success condition |
|---|---|---|---|---|---|---|
| O1 |  |  |  |  |  |  |

## 4. Mandatory constraints

For each constraint, record the source or explicit human judgment and its approved scope.

| ID | Constraint | Input basis | Source IDs | Authority scope | Uncertainty / dissent | Review trigger |
|---|---|---|---|---|---|---|
| MC-1 |  |  |  |  |  |  |

Constraint domains may include:

- legal / jurisdictional;
- safety;
- privacy;
- security;
- organizational;
- accessibility;
- labor;
- affected-party commitment;
- time-window;
- resource;
- other.

## 5. Requirements

Use the form:

> When trigger T occurs, actor or institution A shall perform response R within time W, preserve evidence E, and invoke fallback F if completion cannot be demonstrated.

| ID | Input basis / source IDs | Trigger | Performing actor or system | Accountable owner | Required response | Time window | Evidence | Fallback | Residual condition |
|---|---|---|---|---|---|---|---|---|---|
| R1 |  |  |  |  |  |  |  |  |  |

## 6. Candidate interventions

| ID | Category | Description | Objectives served | Dependencies |
|---|---|---|---|---|
| C1 | organizational / procedural / interface / technical / contractual / institutional / temporal |  |  |  |

## 7. Trade-off analysis

| Criterion | C1 | C2 | C3 | Evidence / uncertainty |
|---|---|---|---|---|
| Pathway benefit |  |  |  |  |
| Timeliness |  |  |  |  |
| Operational burden |  |  |  |  |
| Over-intervention risk |  |  |  |  |
| Power concentration |  |  |  |  |
| Affected-party accessibility |  |  |  |  |
| Privacy / security exposure |  |  |  |  |
| Remaining response options |  |  |  |  |
| Responsibility-theatre risk |  |  |  |  |
| Blame-transfer risk |  |  |  |  |
| Residual harm |  |  |  |  |
| Evidence quality |  |  |  |  |
| Feasibility |  |  |  |  |
| Normative-source fit and conflict |  |  |  |  |
| Authority and scope limit |  |  |  |  |

Do not collapse this table into a total score unless the aggregation rule and value judgments are explicitly justified.

## 8. Selected design

- Selected intervention set:
- Selection rationale:
- Mandatory constraints satisfied:
- Input basis and source trace:
- Rejected alternatives and reasons:
- Unresolved uncertainties:
- Unresolved normative conflicts or dissent:
- Expected burdens:
- Residual risks:
- Residual stewardship owner:
- Review date or trigger:
- Source expiry / supersession triggers:
- Reopening conditions:

## 8A. Responsibility Routing / handoff decision

For consequential handoffs, record **why the next route is permitted**, not merely its destination. Refer to [Responsibility Routing design obligations](../docs/responsibility-routing-design-obligations-v0.1.md).

- Transition / current responsibility holder:
- Proposed next holder and receiver eligibility evidence:
- Receiver capability (distinct from eligibility):
- Required Authority class and existing delegation scope:
- Current effect status (verified / unresolved / unknown / not applicable) and evidence:
- Selected route (bounded continuation / delegated AI resolution / neutral hold / reconciliation hold / bounded Human Return / stop with residue / other with justification):
- Allowed actions:
- Prohibited actions:
- Time limit / expiry / re-evaluation condition:
- Residual owner if the route does not complete:
- Justification including alternatives and unresolved conflicts:

A route selection is not Authority transfer. Effect uncertainty is not success or failure. Repair or readback does not itself renew permission to resume.

## 9. Verification obligations

### Design verification

- Required structural relationships:
- Required specification evidence:
- Source-trace and authority-scope checks:

### Implementation verification

- Implementation artifacts:
- Test or inspection method:
- Acceptance conditions:

### X — Exercise verification

- Scenario / exercise / simulation:
- Participants, including affected-party representation where appropriate:
- Usability and timing measurements:
- Failure and fallback checks:
- Result and limitations (not evaluated / met / not met / mixed):

### O — Operational verification

- Real operating period, population, version and scope (if observed):
- Live operation evidence and deviations:
- Timing, accessibility, monitoring and reopening observations:
- Result and limitations (not evaluated / supported / unsupported / mixed):

### V — Broader contextual validation

- Context and affected-party perspectives assessed (if any):
- Independent comparative / longitudinal / institutional evidence:
- Unresolved legal, social, fairness and organizational questions:
- Result and limitations (not evaluated / supported / unsupported / mixed):

The original label `operational validation` is deprecated because an exercise (X) is not proof of live operation (O) or contextual validity (V). See [D/I/X/O/V vocabulary](../docs/verification-validation-vocabulary-v0.1.md).

## 10. Anti-theatre review

- Can the named authority actually intervene?
- Is intervention possible within the relevant time window?
- Are records connected to correction or remedy?
- Can affected parties access and influence review?
- Does residual ownership include authority and resources?
- Has power moved with responsibility?
- Can nominal closure be reopened?
- Is every normative requirement traceable to an admitted source or explicit human judgment?
- Has any advisory, contested, expired, or ambiguous source been represented as settled or binding?

Findings:

## 11. RPE handoff

- Implementation owner:
- Requirements package:
- Evidence package:
- Normative-source IDs, versions, interpreted obligations, and approved scope:
- Unresolved conflicts and dissent:
- Monitoring triggers:
- Source expiry / supersession / interpretation-change triggers:
- Suspension conditions:
- Rollback / containment conditions:
- Recovery obligations:
- Reopening conditions:
- Constraints and unresolved normative judgments:
- Human or institutional authority for exceptions and interpretation changes:

## 12. Human approval gate

- Reviewer decision:
- Approved scope:
- Approved normative-source inputs:
- Exclusions:
- Unresolved conflicts accepted for further work:
- Approval date:
- Next review trigger:
