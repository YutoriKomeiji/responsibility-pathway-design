# RPD Empirical Validation Protocol v0.1

## Status

This document defines a provisional protocol for studying whether Responsibility Pathway Design (RPD) produces observable and practically meaningful differences in sociotechnical systems.

It is a research protocol, not a certification method, legal test, safety case, or claim that RPD has already been validated.

## 1. Purpose

RPD currently provides:

- a transformation kernel from diagnosed pathway weaknesses to design requirements;
- a pattern and anti-pattern language;
- composition and conflict-resolution rules;
- evaluation, assurance, monitoring, and reopening interfaces.

The next research question is empirical:

> Under what conditions does applying RPD improve the continuity, exercisability, visibility, and repairability of responsibility pathways compared with relevant alternatives?

The protocol is designed to make that question answerable without converting every favorable observation into proof of effectiveness.

## 2. Units of analysis

A study should state its unit of analysis explicitly. Candidate units include:

1. a responsibility-bearing transition;
2. a complete responsibility pathway;
3. a workflow or service;
4. an organizational process;
5. a cross-organizational handoff;
6. an incident and recovery episode;
7. a design-review process;
8. a pattern composition;
9. an assurance and reopening cycle.

Results from one unit must not be silently generalized to another.

## 3. Study families

### 3.1 Retrospective incident reconstruction

Use records from a completed incident to reconstruct:

- the actual pathway;
- authority and capability distribution;
- evidence continuity;
- lost or inaccessible response options;
- repair and residual ownership;
- plausible RPD interventions.

This family supports diagnostic and counterfactual analysis. It does not establish that the proposed redesign would have succeeded.

### 3.2 Prospective design comparison

Compare two or more candidate pathway designs before implementation.

At minimum, include:

- the current or baseline design;
- an RPD-informed design;
- a credible alternative not created merely to be weak.

This family can test traceability, conflict visibility, intervention coverage, and reviewer agreement, but not operational effectiveness by itself.

### 3.3 Controlled simulation or tabletop exercise

Exercise selected designs against predefined scenarios.

Possible observations include:

- time to identify the responsible actor;
- time to exercise stop, escalation, contestation, or recovery authority;
- number of unresolved handoffs;
- evidence completeness;
- disagreement between nominal and exercisable authority;
- recovery and reopening performance.

Simulation findings remain bounded by scenario realism and participant behavior.

### 3.4 Field pilot

Deploy a bounded RPD-informed design in a real workflow with explicit scope, monitoring, fallback, and human authorization.

A field pilot should include:

- a baseline period or comparison group where feasible;
- predeclared metrics and stopping conditions;
- incident and near-miss capture;
- participant and affected-party feedback where ethically and practically appropriate;
- a route for challenge and withdrawal;
- a documented decision on continuation, constraint, redesign, or retirement.

### 3.5 Longitudinal operational study

Observe whether pathway properties remain exercisable over time as personnel, systems, vendors, policies, and operating conditions change.

Longitudinal work is necessary because documentation quality at deployment does not show that responsibility remains connected in operation.

### 3.6 Cross-case comparative study

Compare cases with sufficiently similar purposes or risk structures while preserving contextual differences.

Cross-case studies should not collapse legal, cultural, institutional, or sectoral differences into a single score.

## 4. Core research propositions

The following propositions are provisional and testable.

### P1. Traceability proposition

RPD-informed designs produce a more explicit and reviewable trace from diagnosed finding to objective, requirement, intervention, trade-off, verification obligation, and responsible owner.

### P2. Exercisability proposition

RPD-informed designs reduce the gap between nominal authority and authority that can be exercised within the relevant time window.

### P3. Response-option proposition

RPD-informed designs preserve or deliberately allocate a wider and more appropriate set of response options than designs focused only on approval and logging.

### P4. Recovery proposition

RPD-informed designs identify recovery ownership, resources, and residual stewardship more consistently than baseline designs.

### P5. Anti-theatre proposition

RPD review detects controls that are formally present but operationally inaccessible, delayed, under-resourced, or disconnected.

### P6. Reopening proposition

RPD-informed assurance and monitoring create clearer conditions for challenge, constraint, suspension, redesign, and retirement.

### P7. Burden proposition

RPD introduces additional analytical and operational burden. Its benefits may not justify that burden in every context.

### P8. Context-dependence proposition

The value and form of RPD interventions vary with stakes, reversibility, time pressure, organizational capacity, affected-party access, and institutional setting.

## 5. Outcome dimensions

A study may evaluate the following dimensions, provided each is operationalized separately.

| Dimension | Example observable |
|---|---|
| Pathway legibility | independent reviewers can identify transitions, owners, and gaps |
| Authority–capability alignment | detecting actors can trigger an effective response |
| Intervention timeliness | response occurs before the relevant option expires |
| Evidence continuity | decisions and changes can be reconstructed with bounded uncertainty |
| Returnability | a human or institution can receive responsibility back |
| Contestability | affected or authorized parties can understand and challenge transitions |
| Recovery capacity | correction, restoration, compensation, and reform have assigned resources |
| Residual stewardship | irreducible consequences retain an accountable steward |
| Proportionality | irreversible commitments are justified against purpose and stakes |
| Adaptability | pathway changes trigger review and rebinding |
| Operational burden | time, staffing, cost, friction, and cognitive load |
| Power distribution | interventions alter who can decide, stop, challenge, or recover |

No single dimension should be used as a proxy for all others.

## 6. Baselines and comparators

A credible evaluation must specify what RPD is compared against.

Possible comparators include:

- the current process;
- a standard human-in-the-loop control;
- a conventional RACI or ownership matrix;
- an incident-response or change-control process;
- a systems-safety or assurance method;
- a requirements-engineering review;
- another responsibility or accountability framework;
- a combined method without the RPD transformation layer.

The comparison should explain:

- why the comparator is relevant;
- whether it was implemented competently;
- which purposes overlap and which do not;
- what RPD adds, duplicates, or potentially weakens.

## 7. Pre-registration expectations

Before collecting evaluative data, record:

1. research questions;
2. study family and unit of analysis;
3. inclusion and exclusion criteria;
4. baseline and comparators;
5. propositions being tested;
6. primary and secondary outcomes;
7. evidence sources;
8. analysis method;
9. stopping or withdrawal conditions;
10. known conflicts of interest;
11. privacy, security, legal, and ethical constraints;
12. planned treatment of missing or contradictory evidence.

Exploratory findings should be labeled exploratory rather than retroactively presented as predeclared confirmation.

## 8. Evidence hierarchy

The following hierarchy is descriptive, not automatically cumulative.

- **V0 — Conceptual:** argument, model, or expert judgment only.
- **V1 — Artifact inspection:** trace, requirements, records, or design documents examined.
- **V2 — Structured review:** independent reviewers apply a declared protocol.
- **V3 — Exercise evidence:** simulation, tabletop, drill, or controlled test.
- **V4 — Field evidence:** bounded use in a real operating context.
- **V5 — Longitudinal or comparative evidence:** repeated operation, multiple sites, or credible cross-case analysis.

Higher levels can still contain bias, weak measurement, or unsuitable comparisons. A V5 label is not equivalent to proof, certification, or universal validity.

## 9. Mixed-method design

RPD concerns structures, practices, experiences, and institutional power. Quantitative and qualitative evidence may therefore be combined.

### Quantitative examples

- intervention latency;
- percentage of transitions with identified owners;
- percentage of authorities successfully exercised during tests;
- unresolved escalation count;
- evidence retrieval completeness;
- time to recovery ownership assignment;
- reopening frequency and outcome;
- operational burden and review time.

### Qualitative examples

- interviews with operators, reviewers, managers, and affected parties;
- observation of exercises and incidents;
- explanation of why authority could or could not be exercised;
- analysis of disagreement, workarounds, and hidden dependencies;
- accounts of contestability and residual impact.

Numerical aggregation must not erase materially different experiences or responsibility distributions.

## 10. Reviewer design

Where feasible, use reviewers who are independent from the original design team.

Record:

- reviewer expertise and role;
- training materials;
- access to evidence;
- whether reviewers were blinded to study conditions;
- disagreement and adjudication procedures;
- inter-reviewer agreement where meaningful;
- unresolved interpretive differences.

Agreement is not the same as truth, and disagreement may expose an important ambiguity in the pathway or protocol.

## 11. Negative cases and null results

Studies should actively seek cases where:

- RPD adds no detectable benefit;
- RPD increases delay or burden without proportional gain;
- an alternative method performs equally or better;
- RPD patterns conflict or create new ownership gaps;
- controls pass document review but fail in exercise or operation;
- participants route around the designed pathway;
- affected parties remain unable to challenge or obtain remedy;
- the framework misclassifies a problem or directs attention away from a more important cause.

Null and negative results are part of theory development, not repository failures to hide.

## 12. Confounding and bias controls

Common threats include:

- novelty effects;
- reviewer allegiance;
- selection of unusually weak baselines;
- more time or expertise given to the RPD condition;
- hindsight bias in incident reconstruction;
- outcome knowledge influencing diagnosis;
- incomplete records;
- survivorship and publication bias;
- organizational incentives to present controls as effective;
- underrepresentation of affected parties;
- sector-specific results presented as general.

Each study should document which threats were addressed and which remain.

## 13. Ethical and governance requirements

Empirical work must not use RPD as a reason to bypass existing research ethics, worker consultation, privacy, security, legal, safety, or institutional review requirements.

Where people may be affected, consider:

- meaningful notice and consent where applicable;
- protection against retaliation;
- routes for challenge and withdrawal;
- minimization of sensitive data collection;
- restrictions on publishing operational vulnerabilities;
- separation between research participation and employment evaluation;
- compensation or support for burdens placed on participants.

## 14. Reporting structure

A study report should include:

1. context and purpose;
2. unit of analysis;
3. pathway scope and boundaries;
4. baseline and comparators;
5. research propositions;
6. method and evidence level;
7. findings by outcome dimension;
8. contradictory and missing evidence;
9. negative cases and burden;
10. limitations and transfer conditions;
11. changes made during the study;
12. human authorization and governance decisions;
13. data and artifact availability;
14. claims that the study does not support.

## 15. Minimum claim discipline

Acceptable bounded language includes:

- “In this exercise, the RPD-informed design reduced median escalation latency.”
- “Reviewers identified more explicit recovery ownership in the RPD condition.”
- “No operational effectiveness claim is supported because the design was not field-tested.”
- “The intervention improved traceability but increased review burden.”

Avoid language such as:

- “RPD proves responsibility.”
- “RPD guarantees accountability.”
- “The framework is validated” without specifying scope, method, evidence level, and limitations.
- “RPD is superior” based on a single weak or artificial comparator.

## 16. Exit and reopening

A study conclusion should state whether the evidence supports:

- further conceptual revision;
- additional exercise;
- bounded field pilot;
- continued operation with monitoring;
- constraint or suspension;
- redesign;
- retirement of a pattern, metric, or proposition.

Unexpected evidence should be routed back to the transformation kernel, pattern language, composition rules, or assurance interface rather than treated only as a reporting problem.

## 17. Research boundary

This protocol establishes a way to ask better empirical questions. It does not itself provide empirical validation, certify an implementation, resolve legal liability, or prove safety, fairness, compliance, effectiveness, or social acceptance.
