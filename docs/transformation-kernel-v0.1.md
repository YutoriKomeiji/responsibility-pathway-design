# RPD Transformation Kernel v0.1

## Purpose

Responsibility Pathway Design (RPD) translates a diagnosed responsibility-pathway weakness or an explicitly authorized normative input into a reviewable design response.

The kernel defines a minimum transformation sequence:

```text
RPM finding and/or admitted normative-source input
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

An RPD transformation begins only when the input contains enough information to distinguish a supported finding, an authorized normative source, and a provisional assumption.

### 1.1 RPM-finding input

Minimum RPM-finding fields:

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

### 1.2 Normative-source input

A design obligation may also enter through an admitted normative source, including a law, regulation, contract, approved policy, standard, governance decision, affected-party commitment, or other explicitly authorized source.

Each normative input must preserve:

- a stable source identifier and version;
- source type and issuing authority;
- citation and applicable scope;
- binding, advisory, contested, expired, or unknown status;
- the interpreted obligation, separately from the source text;
- the named human or institutional interpretation owner;
- uncertainty, dissent, conflicts, and affected-party burdens;
- approval status for the stated transformation;
- expiry, supersession, review, and reopening triggers.

The detailed admission, conflict, and non-transfer rules are defined in the [Normative-Source Input Contract v0.1](./normative-source-input-contract-v0.1.md).

A normative source must not be converted into a fictitious RPM finding. An RPM finding must not be rewritten as a binding legal, ethical, policy, or affected-party conclusion without an authorized source or decision process.

### 1.3 Input-basis classification

Each design objective and mandatory constraint must be classified as:

- `RPM-derived`;
- `normative-source-derived`;
- `combined`;
- `design assumption`;
- `human judgment`.

Provisional assumptions and human judgments require a named owner, rationale, bounded scope, and review trigger.

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

A single RPM finding may map to more than one class. Normative-source inputs are not finding classes; they constrain objectives, requirements, selection, verification, or authorization.

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

A normative-source-derived objective must identify the admitted source, interpreted obligation, authority scope, and approval record. Citation alone is not sufficient.

## 4. Requirement derivation

A design requirement must be testable and must identify:

- the triggering condition;
- the performing actor or system;
- the accountable human or institutional owner;
- the required response;
- the allowed time window;
- the evidence to be produced;
- the escalation or fallback path;
- the residual condition if the response fails;
- its input basis and source identifiers.

Recommended form:

> When **trigger T** occurs, **actor or institution A** shall perform **response R** within **time W**, preserve **evidence E**, and invoke **fallback F** if completion cannot be demonstrated.

A requirement is incomplete if it names a control without identifying who can exercise it or how effectiveness will be evidenced.

A quotation, policy statement, or general value is not yet a design requirement. It must be interpreted, approved, and translated into testable terms without expanding its authority.

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
- implementation feasibility;
- normative-source fit, conflict, and authority limits where applicable.

RPD does not optimize a single score by default. A scalar score may conceal incompatible values and affected-party burdens.

## 7. Selection rule

A selected design should satisfy all mandatory constraints and provide a documented rationale for rejected alternatives.

Selection must record:

- chosen intervention set;
- design objective served;
- mandatory constraints and their input basis;
- expected benefits;
- expected burdens;
- rejected alternatives and reasons;
- unresolved uncertainty;
- unresolved normative conflict or dissent;
- residual risk and stewardship owner;
- review and reopening conditions.

A design may legitimately preserve an irreversible transition when irreversibility is necessary, proportionate, authorized, evidenced, contestable where applicable, and paired with residual stewardship.

When normative sources conflict, RPD may prepare alternatives but must not silently choose a hierarchy. The authorized human or institutional decision, rationale, dissent, and reopening trigger must be recorded.

## 8. Verification obligation

Every selected design must produce verification obligations at three levels.

### Design verification

Does the design specification contain the required authority, trigger, evidence, fallback, ownership, and source-trace relationships?

### Implementation verification

Was the approved design implemented as specified?

### Operational validation

Can authorized people and institutions actually exercise the designed response under realistic conditions?

Formal or technical verification alone does not establish operational validation, legal adequacy, normative correctness, or social legitimacy.

For normative-source-derived requirements, verification must also detect source expiry, supersession, interpretation change, unresolved conflict, and operation beyond the approved scope.

## 9. Anti-theatre checks

A design must be challenged with at least these questions:

- Is the named human or institution able to intervene, or merely present?
- Is the escalation path usable within the actual harm window?
- Are records linked to remedy, or only retained?
- Can affected parties initiate review without prohibitive cost or expertise?
- Does residual ownership include resources and authority?
- Does the design move blame downstream without moving power?
- Can the pathway be reopened after nominal closure?
- Is each normative requirement traceable to an admitted source or explicit human judgment?
- Has an advisory, contested, expired, or ambiguous source been represented as settled or binding?

## 10. RPE handoff

The minimum handoff package contains:

- transformation identifier and version;
- source RPM finding identifiers;
- admitted normative-source identifiers and versions;
- interpreted obligations, approval status, authority scope, uncertainty, and dissent;
- design objectives;
- testable requirements;
- selected interventions;
- implementation owners;
- evidence requirements;
- verification conditions;
- monitoring triggers;
- source expiry, supersession, and interpretation-change triggers;
- suspension, rollback, recovery, and reopening conditions;
- rejected alternatives;
- residual risk and stewardship ownership;
- legal, privacy, security, organizational, and jurisdictional constraints.

RPE may implement and check this package. It must not reinterpret unresolved normative judgments as technically settled facts or expand a source beyond its approved scope.

## 11. Research status

This kernel is a provisional design-method artifact. It requires comparative cases, independent coding, counterexamples, and evaluation against strong combinations of existing governance and engineering practices. The normative-source contract does not provide legal advice, establish a universal source hierarchy, or certify compliance or ethical adequacy.
