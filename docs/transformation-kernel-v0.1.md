# RPD Transformation Kernel v0.1

## Purpose

Responsibility Pathway Design (RPD) translates a diagnosed responsibility-pathway weakness into a reviewable design response.

The kernel defines a minimum transformation sequence:

```text
RPM finding
  -> design objective
  -> design requirement
  -> candidate interventions
  -> trade-off evaluation
  -> selected design
  -> verification obligation
  -> RPE handoff
```

This sequence is not a guarantee of safety, fairness, legality, or successful recovery. It is a disciplined way to make design reasoning inspectable.

## 1. Input contract

An RPD transformation begins only when the input contains enough information to distinguish a supported finding from an assumption.

Minimum input fields:

- pathway identifier;
- transition or transition set;
- affected state change;
- actors, roles, and institutions;
- authority and capability distribution;
- evidence basis;
- uncertainty status;
- affected parties;
- available and unavailable response options;
- relevant intervention window;
- residual impact;
- current ownership or ownership gap.

If the evidence status is `unknown`, RPD must preserve that uncertainty. It must not silently convert missing evidence into a confirmed defect.

## 2. Finding classes

The initial kernel uses eight finding classes.

### F1. Authority-capability mismatch

An actor can detect, understand, or influence a transition but lacks exercisable authority to intervene within the relevant time window.

### F2. Evidence discontinuity

The rationale, approval basis, scope, execution record, or recovery record cannot be reconstructed across a transition.

### F3. Scope discontinuity

The approved, tested, monitored, or remediated scope does not match the actual affected scope.

### F4. Return-point failure

A pathway cannot return to a competent human or institutional decision point when automation, delegation, or organizational handoff becomes unreliable.

### F5. Contestation failure

Affected parties cannot access, understand, initiate, or meaningfully influence review and correction.

### F6. Recovery ownership failure

Technical restoration may be possible, but correction, compensation, explanation, institutional repair, or residual stewardship has no effective owner.

### F7. Assumption expiry failure

A pathway continues to operate after a material assumption, authorization, model condition, data condition, or organizational premise has expired.

### F8. Cross-boundary handoff failure

Responsibility becomes ambiguous or non-exercisable when work crosses teams, organizations, jurisdictions, vendors, or autonomous agents.

A single RPM finding may map to more than one class.

## 3. Design objective derivation

A design objective describes the pathway property to be preserved or restored. It should not prematurely select a specific mechanism.

Examples:

| Finding class | Candidate design objectives |
|---|---|
| F1 | preserve timely intervention; align authority with capability; provide bounded escalation |
| F2 | preserve evidence continuity; bind decisions to execution and recovery records |
| F3 | align approval, test, monitoring, and remediation scope |
| F4 | preserve competent human or institutional returnability |
| F5 | make contestation accessible, timely, intelligible, and consequential |
| F6 | assign and resource recovery and residual stewardship |
| F7 | expire or revalidate assumptions before continuation |
| F8 | preserve responsibility across contractual, organizational, and technical boundaries |

Objectives must be stated as pathway properties, not as slogans such as "increase accountability".

## 4. Requirement derivation

A design requirement must be testable and must identify:

- the triggering condition;
- the performing actor or system;
- the accountable human or institutional owner;
- the required response;
- the allowed time window;
- the evidence to be produced;
- the escalation or fallback path;
- the residual condition if the response fails.

Recommended form:

> When **trigger T** occurs, **actor or institution A** shall perform **response R** within **time W**, preserve **evidence E**, and invoke **fallback F** if completion cannot be demonstrated.

A requirement is incomplete if it names a control without identifying who can exercise it or how effectiveness will be evidenced.

## 5. Candidate intervention generation

RPD should generate more than one intervention candidate where feasible.

Candidate categories include:

- organizational: role redesign, authority reassignment, independent review;
- procedural: escalation, dual approval, staged commitment;
- interface: warning, pause, confirmation, explanation, contestation access;
- technical: containment, rollback, version pinning, evidence capture;
- contractual: handoff obligations, recovery ownership, evidence retention;
- institutional: appeal body, compensation process, reopening authority;
- temporal: time-bounded delegation, assumption expiry, scheduled revalidation.

The kernel does not treat technical controls as automatically superior to organizational or institutional controls.

## 6. Trade-off evaluation

Each candidate should be evaluated against at least:

- expected pathway benefit;
- timeliness;
- operational burden;
- false-positive or over-intervention risk;
- power concentration;
- accessibility to affected parties;
- privacy and security exposure;
- reversibility and remaining response options;
- responsibility-theatre risk;
- blame-transfer risk;
- residual harm;
- evidence quality;
- implementation feasibility.

RPD does not optimize a single score by default. A scalar score may conceal incompatible values and affected-party burdens.

## 7. Selection rule

A selected design should satisfy all mandatory constraints and provide a documented rationale for rejected alternatives.

Selection must record:

- chosen intervention set;
- design objective served;
- mandatory constraints;
- expected benefits;
- expected burdens;
- rejected alternatives and reasons;
- unresolved uncertainty;
- residual risk and stewardship owner;
- review and reopening conditions.

A design may legitimately preserve an irreversible transition when irreversibility is necessary, proportionate, authorized, evidenced, contestable where applicable, and paired with residual stewardship.

## 8. Verification obligation

Every selected design must produce verification obligations at three levels.

### Design verification

Does the design specification contain the required authority, trigger, evidence, fallback, and ownership relationships?

### Implementation verification

Was the approved design implemented as specified?

### Operational validation

Can authorized people and institutions actually exercise the designed response under realistic conditions?

Formal or technical verification alone does not establish operational validation or social legitimacy.

## 9. Anti-theatre checks

A design must be challenged with at least these questions:

- Is the named human or institution able to intervene, or merely present?
- Is the escalation path usable within the actual harm window?
- Are records linked to remedy, or only retained?
- Can affected parties initiate review without prohibitive cost or expertise?
- Does residual ownership include resources and authority?
- Does the design move blame downstream without moving power?
- Can the pathway be reopened after nominal closure?

## 10. RPE handoff

The minimum handoff package contains:

- transformation identifier and version;
- source RPM finding identifiers;
- design objectives;
- testable requirements;
- selected interventions;
- implementation owners;
- evidence requirements;
- verification conditions;
- monitoring triggers;
- suspension, rollback, recovery, and reopening conditions;
- rejected alternatives;
- residual risk and stewardship ownership;
- legal, privacy, security, organizational, and jurisdictional constraints.

RPE may implement and check this package. It must not reinterpret unresolved normative judgments as technically settled facts.

## 11. Research status

This kernel is a provisional design-method artifact. It requires comparative cases, independent coding, counterexamples, and evaluation against strong combinations of existing governance and engineering practices.
