# RPD Evaluation Protocol v0.1

## Status

This is a provisional protocol for evaluating Responsibility Pathway Design (RPD) artifacts. It supports structured review and comparative research. It is not a certification method and does not establish safety, legality, compliance, fairness, effectiveness, or social acceptance.

## Purpose

RPD requires evaluation at more than one level. A design may be internally coherent but not implemented. It may be implemented but not exercisable. It may be exercisable in tests but inaccessible to affected parties. It may function operationally while still producing unacceptable residual harm.

The protocol therefore separates:

1. diagnostic adequacy;
2. design coherence;
3. implementation verification;
4. operational verification;
5. real-world validation;
6. residual-impact and governance review.

## Evaluation object

An evaluation should identify the exact object under review:

- a single pattern;
- a composed pattern set;
- a pathway segment;
- an end-to-end pathway;
- a cross-organizational pathway;
- a revision after incident or policy change.

The unit of evaluation must not shift silently during review.

## Evidence classes

Evidence should be classified before conclusions are drawn.

### E0 — assertion

A claim or intended behavior without supporting artifact or observation.

### E1 — design artifact

Requirements, diagrams, decisions, pattern records, contracts, or procedures.

### E2 — implementation evidence

Configuration, code, access control, workflow state, interface behavior, or deployment record.

### E3 — exercise evidence

Test, simulation, tabletop exercise, failure injection, or controlled rehearsal.

### E4 — operational evidence

Observed behavior in real operation, including incidents, overrides, appeals, recovery, and monitoring.

### E5 — independent or affected-party evidence

Independent review, audit, user study, complaint record, affected-party testimony, external replication, or equivalent evidence.

Higher evidence classes do not automatically validate broader claims. Scope and relevance must still be established.

## Evaluation dimensions

### 1. Diagnostic traceability

Questions:

- Can each design objective be traced to an RPM finding or an explicit normative requirement?
- Are uncertainty and missing evidence preserved?
- Are affected parties and time windows represented?
- Are lost or weakened response options identified?

Failure condition:

- the design introduces controls without showing which pathway weakness they address.

### 2. Requirement quality

Questions:

- Is each requirement testable?
- Does it specify scope, trigger, actor, timing, evidence, and expected outcome where relevant?
- Does it avoid vague terms such as appropriate, timely, or sufficient without criteria?
- Are exceptions bounded?

Failure condition:

- a requirement can be declared satisfied without observable evidence.

### 3. Pattern fit

Questions:

- Does the selected pattern match the diagnosed failure structure?
- Were alternatives considered?
- Are applicability conditions met?
- Are known trade-offs and failure modes recorded?

Failure condition:

- a familiar pattern is selected because it is available rather than because it fits.

### 4. Composition coherence

Questions:

- Are dependencies, sequencing, parallel branches, overrides, substitutions, and conflicts explicit?
- Are composition invariants satisfied?
- Are interface failures tested?
- Can local exceptions collectively defeat the intended pathway property?

Failure condition:

- individual patterns pass review while the composition fails as a whole.

### 5. Authority–capability alignment

Questions:

- Can the responsible actor exercise the assigned authority?
- Does the actor have access, time, information, staffing, and organizational protection?
- Is escalation available before the intervention window expires?
- Can authority be exercised against routine pressure or senior preference?

Failure condition:

- authority exists nominally but cannot be used in practice.

### 6. Evidence continuity

Questions:

- Are decisions, assumptions, overrides, revisions, and closures reconstructable?
- Are records correlated across organizations and systems?
- Are retention, integrity, access, privacy, and deletion rules defined?
- Is evidence available to the actors who need it?

Failure condition:

- logs exist but cannot support explanation, contestation, repair, or review.

### 7. Contestability and accessibility

Questions:

- Can affected parties understand that a pathway transition occurred?
- Can they challenge, appeal, request correction, or obtain explanation?
- Are routes usable under real constraints such as language, disability, cost, time, and power imbalance?
- Does contestation pause or alter consequential action where justified?

Failure condition:

- a formal route exists but is practically inaccessible.

### 8. Recovery completeness

Questions:

- Does recovery distinguish stop, contain, undo, correct, restore, compensate, explain, contest, reform, reopen, and steward residue?
- Is recovery ownership assigned?
- Are nontechnical consequences included?
- Is closure conditional on evidence rather than administrative declaration?

Failure condition:

- technical restoration is treated as complete recovery.

### 9. Residual stewardship

Questions:

- What cannot be undone?
- Who remains responsible after technical closure?
- Are monitoring, compensation, care, reform, or long-term obligations defined?
- Are reopening triggers present?

Failure condition:

- irreversible or persistent impact loses ownership after incident closure.

### 10. Proportionality and burden

Questions:

- Is the degree of control proportionate to stakes and uncertainty?
- Does the design create harmful delay, exclusion, surveillance, or concentration of power?
- Are burdens distributed fairly enough to warrant further validation?
- Are less burdensome alternatives documented?

Failure condition:

- pathway protection is asserted without reviewing the harms introduced by the protection itself.

### 11. Anti-theatre robustness

Questions:

- Can the control be exercised under pressure?
- Has it been tested with realistic failure conditions?
- Are incentives aligned with use?
- Can an actor bypass it without detection?
- Does the evidence show operation rather than mere presence?

Failure condition:

- documentation is used as a substitute for exercisability.

### 12. Adaptation and reopening

Questions:

- Are assumptions versioned and time-bounded?
- Are monitoring thresholds and review dates defined?
- Can affected evidence reopen a closed decision?
- Does the pathway adapt to organizational, model, legal, or environmental change?

Failure condition:

- a design remains authoritative after its assumptions expire.

## Evaluation levels

### Level D — design review

Minimum evidence: E1.

Determines whether the design is traceable, coherent, bounded, and reviewable.

It does not establish implementation or operation.

### Level I — implementation verification

Minimum evidence: relevant E2.

Determines whether specified controls and interfaces were implemented as designed.

It does not establish exercisability under pressure.

### Level X — exercise verification

Minimum evidence: E3.

Determines whether the pathway can be exercised in controlled scenarios, including negative and failure cases.

It does not establish routine or affected-party effectiveness.

### Level O — operational verification

Minimum evidence: E4.

Determines whether the pathway operated in real conditions over a stated period and scope.

It does not by itself establish social legitimacy or absence of harm.

### Level V — broader validation

Minimum evidence: relevant E4 and E5.

Examines whether the design contributes to the intended real-world responsibility outcomes for affected parties and institutions.

This level requires explicit methods, comparison, scope limits, and independent scrutiny.

## Rating language

Use bounded conclusions:

- not evaluated;
- insufficient evidence;
- design criterion met / not met;
- implementation verified / not verified;
- exercised successfully / unsuccessfully under stated conditions;
- operational evidence supports / does not support the stated claim;
- validation question remains open;
- mixed or conflicting evidence.

Avoid unqualified labels such as safe, responsible, compliant, fair, effective, or validated.

## Comparative evaluation

A comparative study should include:

- the RPD-informed design;
- at least one credible baseline;
- comparable context and stakes;
- predefined outcome and process measures;
- negative outcomes and burden measures;
- evidence quality assessment;
- alternative explanations;
- scope and transfer limits.

Possible baselines include:

- existing organizational process;
- standard human-in-the-loop control;
- logging-only control;
- conventional incident response;
- established safety, assurance, governance, or requirements method;
- an integrated baseline combining several established methods.

RPD should not be compared only with a deliberately weak baseline.

## Minimum test set for a composed design

A review should include, where relevant:

1. normal-path test;
2. delayed-response test;
3. unavailable-owner test;
4. conflicting-authority test;
5. evidence-loss test;
6. unauthorized-bypass test;
7. exception-cascade test;
8. affected-party contestation test;
9. rollback-with-residual-harm test;
10. cross-organization handoff failure;
11. expired-assumption test;
12. reopening test.

## Evaluation record

Each evaluation should record:

- object and scope;
- evaluator and conflicts of interest;
- date and version;
- claims under review;
- evidence inventory and class;
- methods and scenarios;
- dimension-by-dimension findings;
- unmet criteria;
- observed failures;
- residual uncertainty;
- comparison limits;
- required remediation;
- monitoring and reopening conditions;
- approval status.

## Human judgment boundary

RPD evaluation can structure evidence and disagreement. It cannot eliminate normative judgment, legal interpretation, domain expertise, affected-party participation, or accountable human approval.

## Research agenda

- inter-rater reliability of RPD evaluations;
- domain-specific adaptations;
- evidence thresholds for exercisability;
- measurement of contestability and recovery completeness;
- comparison with established governance and assurance methods;
- longitudinal evidence on residual stewardship;
- detection of responsibility theatre;
- methods for affected-party participation without tokenism.

## Boundary statement

This protocol is a research scaffold. Its criteria require testing, refinement, counterexamples, independent review, and empirical validation before stronger claims are justified.