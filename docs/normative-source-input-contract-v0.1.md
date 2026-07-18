# RPD Normative-Source Input Contract v0.1

## Status and purpose

This document defines how an explicit normative source may enter Responsibility Pathway Design (RPD) when a design obligation cannot be derived solely from an RPM finding.

It is a bounded input contract. It does not authorize RPD to create law, policy, ethics, institutional mandates, affected-party preferences, or social legitimacy. It makes the provenance, authority, interpretation, uncertainty, conflict, and approval status of a normative input inspectable.

## Why a separate contract is needed

RPM findings describe responsibility-pathway conditions and weaknesses. Some design constraints arise from external normative sources, including:

- law, regulation, and binding administrative requirements;
- contracts and formally delegated obligations;
- organizational policies and approved governance decisions;
- professional, sectoral, or technical standards;
- safety, security, privacy, labor, accessibility, or human-rights requirements;
- decisions of an authorized oversight, appeal, ethics, or affected-party body;
- documented commitments to affected parties;
- other explicitly approved normative sources.

These sources differ in authority, scope, interpretation, enforceability, and revision process. They must not be collapsed into an undifferentiated label such as `compliance requirement` or silently represented as an RPM diagnosis.

## Two authorized input paths

An RPD transformation may begin from either or both of the following:

```text
Path A: RPM finding
  observed or reconstructed responsibility-pathway condition

Path B: authorized normative-source input
  externally grounded obligation, prohibition, permission, value constraint,
  procedural requirement, or affected-party commitment
```

The two paths are related but non-equivalent.

- An RPM finding does not by itself establish that a particular normative rule is legally or ethically required.
- A normative source does not by itself establish that a pathway weakness exists in practice.
- A single RPD design may need both: an RPM finding to describe the pathway problem and a normative source to constrain the acceptable response.

## Minimum normative-source record

Each normative-source input must record at least:

| Field | Required content |
|---|---|
| Normative source ID | stable, versioned identifier |
| Source type | law, regulation, contract, policy, standard, governance decision, affected-party commitment, or other declared type |
| Issuing authority | named institution, body, role, or authorized process |
| Source citation | title, section, version, date, and retrievable reference where permitted |
| Jurisdiction or domain | legal, organizational, contractual, sectoral, geographic, or affected scope |
| Binding status | binding, contractually binding, internally mandatory, advisory, contested, proposed, expired, or unknown |
| Effective period | start date, expiry, review date, supersession status, or unknown |
| Interpreted obligation | bounded statement of the obligation, prohibition, permission, or value constraint |
| Interpretation owner | named human or institutional role responsible for the interpretation |
| Interpretation method | legal advice, policy decision, standards mapping, affected-party process, expert review, or other method |
| Uncertainty and dissent | ambiguity, competing interpretation, minority view, challenge, or unresolved question |
| Affected parties | groups or persons whose interests, rights, access, or burdens are implicated |
| Conflict relationships | conflicting, overlapping, or dependent sources and the rule for handling them |
| Approval status | proposed, reviewed, approved for this transformation, suspended, superseded, or rejected |
| Review and reopening trigger | change in law, policy, contract, evidence, impact, authority, or affected-party challenge |

A source is not ready for design use when its authority, scope, interpreted obligation, or approval status is materially unknown.

## Source-authority classes

RPD may use a local classification to prevent accidental equivalence among sources.

| Class | Example | What the class does not establish |
|---|---|---|
| N1 — externally binding | applicable law, regulation, court or regulator order | correct interpretation, complete compliance, or legal sufficiency |
| N2 — contractually or institutionally binding | contract, approved internal policy, delegated decision | external legality, legitimacy, or practical adequacy |
| N3 — recognized standard or professional norm | technical, safety, professional, or sector standard | universal applicability or certification |
| N4 — authorized affected-party or oversight commitment | approved remedy agreement, consultation outcome, appeal or oversight decision | representation of every affected party or absence of power imbalance |
| N5 — advisory or proposed source | guidance, recommendation, draft policy, research-based proposal | binding status or final organizational approval |

These classes describe source status only. They are not quality scores and must not be automatically ranked across contexts.

## Admission rule

A normative source may constrain an RPD transformation only when:

1. the source is identifiable and versioned;
2. its issuing authority and applicable scope are recorded;
3. the interpreted obligation is stated separately from the source text;
4. interpretation uncertainty and dissent are preserved;
5. a named human or institutional authority approves its use for the stated transformation;
6. conflicts with other sources are visible;
7. expiry, supersession, and reopening conditions are defined;
8. the source does not require RPD to claim legal, ethical, social, or affected-party conclusions beyond the available authority and evidence.

Failure to meet these conditions results in `normative input not admitted`, `admitted with unresolved uncertainty`, or `human decision required` rather than silent inclusion.

## Separation of source, interpretation, and design requirement

The following objects must remain distinct:

```text
Normative source
  → interpreted obligation
  → approved RPD constraint or objective
  → testable design requirement
  → implementation and evidence obligation
```

A quotation or citation is not yet a design requirement. A design requirement must still identify trigger, actor or system, accountable owner, response, time window, evidence, fallback, and residual condition.

## Relationship to RPM findings

For each design objective or mandatory constraint, record one of:

- `RPM-derived` — traceable to one or more RPM findings;
- `normative-source-derived` — traceable to one or more admitted normative sources;
- `combined` — supported by both;
- `design assumption` — not yet supported by either and therefore explicitly provisional;
- `human judgment` — a bounded decision whose authority and rationale are recorded.

A normative source must not be converted into a fictitious RPM finding. An RPM finding must not be rewritten as a binding normative conclusion without an authorized source or decision process.

## Conflict and priority handling

When sources conflict, RPD must not resolve the conflict by convenience, technical feasibility, or an unrecorded hierarchy.

The record must identify:

- the conflicting sources and interpretations;
- the authority claimed by each source;
- the applicable scope and time period;
- whether a legally or institutionally authorized priority rule exists;
- affected-party burdens under each interpretation;
- interim containment or suspension conditions;
- the named human or institutional decision authority;
- the decision, rationale, dissent, and reopening trigger.

Until an authorized decision is recorded, the conflict remains unresolved. RPD may prepare alternatives but must not represent one as mandatory.

## Change, expiry, and supersession

A normative-source input must be reopened when:

- the source is amended, repealed, expired, suspended, or superseded;
- jurisdiction, contract, system scope, or affected population changes;
- an authoritative interpretation changes;
- a challenge, appeal, complaint, or affected-party process produces material counterevidence;
- implementation reveals an unanticipated conflict or burden;
- the approving authority loses or changes its mandate.

RPE must not continue treating an expired or superseded normative input as settled. Assurance must treat stale authority or interpretation as a defeater or unresolved assumption. Operational governance must authorize any continuation, constraint, suspension, redesign, or retirement response.

## Prohibited shortcuts

RPD must not:

- invent a legal, policy, ethical, or affected-party requirement;
- treat a general value statement as a testable requirement without interpretation and approval;
- treat an advisory source as binding without declared authority;
- hide disagreement by selecting one interpretation without a decision record;
- use `best practice`, `responsible`, `fair`, `safe`, or `compliant` as a substitute for a cited and scoped source;
- infer affected-party consent from silence or administrative participation;
- treat technical feasibility as authority to narrow a normative obligation;
- treat implementation success as proof that the normative interpretation was correct;
- allow an AI system to become the final authority for legal, ethical, policy, or affected-party judgment.

## Handoff requirements

An RPD-to-RPE package containing normative-source-derived requirements must include:

- normative source IDs and versions;
- admitted interpretation and approval record;
- binding-status and scope statement;
- unresolved conflicts and dissent;
- implementation constraints;
- required evidence of conformance;
- review, expiry, supersession, and reopening triggers;
- the human or institutional authority for interpretation changes and exceptions.

RPE may implement the approved requirement. It may not reinterpret the source as settled beyond the approved scope.

## Evaluation questions

A reviewer should ask:

- Is every normative requirement traceable to an admitted source or explicit human judgment?
- Are source authority, scope, version, and binding status visible?
- Is the interpretation separated from the source itself?
- Are uncertainty, dissent, and affected-party burdens preserved?
- Are conflicts resolved by an authorized process rather than convenience?
- Are expiry and supersession operationally detectable?
- Can a requirement be reopened when authority, interpretation, evidence, or impact changes?
- Does the record avoid implying certification, legal sufficiency, ethical correctness, or social legitimacy?

## Research and authority boundary

This contract is a provisional research artifact. It does not provide legal advice, establish a universal hierarchy of normative sources, determine which law or policy applies, certify compliance, resolve ethical disagreement, or substitute for affected-party participation and accountable human or institutional judgment.
