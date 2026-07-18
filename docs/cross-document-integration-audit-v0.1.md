# RPD Cross-Document Integration Audit and Traceability Matrix v0.1

## Status and scope

This audit reviews the public research surface merged through RPD pull requests #8–#15 at main commit `8dd50f9a43fa8accbad9193832a607423ea530ea`. It covers the transformation kernel, patterns and anti-patterns, composition, evaluation, assurance, operation and reopening, empirical validation and falsification, worked cases, case corpus and coding, entry pages, templates, and examples.

The audit separates observed facts, interpretations, and proposed responses. It does not make a certification, legal, safety, fairness, effectiveness, standardization, or publication decision.

## Severity summary

| Severity | Count | Disposition |
|---|---:|---|
| Critical | 0 | none identified |
| High | 8 | four low-risk corrections implemented; four boundary or method issues documented for review |
| Medium | 9 | bounded terminology, ownership, template, and navigation fixes implemented where non-conceptual |
| Low | 4 | consistency and maintainability items recorded |

## Critical findings

No contradiction was found that invalidates the full theory surface or requires destructive removal.

## High findings

### H1 — Worked-case finding identifiers conflicted with the transformation kernel

- Fact: the benefit-review worked case used `F1`–`F6` with meanings that did not match the kernel finding classes.
- Interpretation: the collision could propagate incorrect coding into case and corpus records.
- Response: separated case-local `BF-*` identifiers from explicit candidate kernel-class mappings and added stable case metadata. This avoids presenting an ambiguous mapping as canonical.

### H2 — Verification and validation stages use conflicting labels

- Fact: the kernel uses design verification, implementation verification, and operational validation; the evaluation protocol separates D, I, X, O, and V; assurance separately names design, implementation, exercise, operation, and broader validation.
- Interpretation: a realistic exercise can be called operational validation in one document and exercise verification in another.
- Proposal: retain the five-stage evaluation model as the reference crosswalk below. Renaming or changing the kernel stage requires a theory decision and was not implemented.

### H3 — Normative requirements are accepted by evaluation but not defined as a kernel input

- Fact: evaluation permits trace to an RPM finding or explicit normative requirement, while the kernel and minimal assurance trace begin with an RPM finding.
- Interpretation: legal, policy, ethical, or affected-party constraints lack a declared source-authority and uncertainty contract.
- Proposal: consider an additional, explicitly authorized normative-source input path. This is a theory-boundary decision and was not implemented.

### H4 — RPE, assurance, and operational governance boundaries differ

- Fact: entry pages include operation within RPE; the assurance interface places monitoring after RPE specification and implementation.
- Interpretation: responsibility for monitoring signals, state-transition authorization, and redesign return can be unclear.
- Proposal: use the responsibility-boundary table below as an interim interface map. Changing the theory stack wording requires human review.

### H5 — Research artifacts were unreachable from all public entry points

- Fact: README, START-HERE, and the Pages index omitted the empirical, falsification, worked-package, corpus, and coding surface.
- Interpretation: methods and templates existed without a discoverable end-to-end route.
- Response: added bounded reading paths to all three entry points.

### H6 — End-to-end case artifact identifiers were incomplete

- Fact: case, corpus, observation, and result templates did not share sufficient stable identifiers and versions.
- Interpretation: a worked case could not be joined deterministically to observations and reports.
- Response: added case, corpus, observation-log, and report identity fields and artifact references.

### H7 — Excluded cases and independent adjudication could not be preserved

- Fact: the corpus protocol requires exclusion records and the coding manual requires original independent decisions and minority interpretations; the manifest did not provide those records.
- Interpretation: selection bias or disagreement could be erased by the data structure.
- Response: added exclusion and quarantine records to the manifest and a case coding and adjudication record template.

### H8 — Operational trigger and period records lacked required controls

- Fact: the operational protocol requires escalation destination, maximum response time, evidence preservation, period observations, state transitions, and human decisions. The assurance template recorded only part of that plan.
- Interpretation: reopening could be declared without a reconstructable operational record.
- Response: expanded assurance trigger fields and added an operational monitoring and reopening log.

## Medium findings

| ID | Fact | Interpretation | Response |
|---|---|---|---|
| M1 | Kernel findings, falsification classes, defeaters, assurance levels, and adjudication outcomes reuse short prefixes. | Cross-document references can be ambiguous. | Use qualified namespaces in new artifacts; see terminology table. Existing IDs were not globally renamed. |
| M2 | E0–E5, D/I/X/O/V, A0–A5, V0–V5, and corpus evidence tiers are distinct axes. | Similar numbering can be mistaken for a convertible maturity score. | Declared non-equivalence in the crosswalk below. |
| M3 | The assurance interface said the framework itself retained responsibility. | A framework cannot be the accountable actor. | Replaced with the named human or institutional design authority applying the method. |
| M4 | Kernel requirements allowed an obligated system without a separate accountable owner. | A system-only obligation can hide human or institutional ownership. | Split performing actor/system from accountable owner. |
| M5 | A stale start page presented RPD as hierarchically above neighboring methods. | This could be read as replacement or superiority. | Marked it historical and clarified complementarity. |
| M6 | The principles appeared to require reversibility in every case. | This conflicted with justified irreversibility and residual stewardship. | Added remaining-response-option and residual-stewardship language. |
| M7 | Source provenance, conflicts, withdrawal, evidence retention, and supersession fields were incomplete. | Protocol requirements could be lost at template handoff. | Added fields to the corpus, empirical-study, assurance, and evaluation templates. |
| M8 | Boundary and inconclusive results were not named consistently across all records. | Binary reporting pressure could hide non-favorable or unresolved cases. | Expanded the manifest classification and documented the common result enum below. |
| M9 | No repository Markdown-lint baseline exists; a default run reports mostly table and line-length style issues. | Raw issue counts are not a useful semantic gate. | Record the check result; defer lint policy selection to maintainers. |

## Low findings

| ID | Finding | Disposition |
|---|---|---|
| L1 | Claim, counterevidence, defeater, trigger, and reopening decision definitions are distributed. | Consolidated a minimal terminology table below. |
| L2 | Repeated catalog subheadings produce generated-anchor suffixes. | No current explicit anchor is broken; retain as a maintainability item. |
| L3 | One worked example omitted the filename version in its H1. | Corrected. |
| L4 | Some framework and review-note files are intentionally outside the main reading graph. | Do not link automatically; maintainers should declare archival or internal-review status when appropriate. |

## Cross-document traceability matrix

| Lifecycle object | Primary authority | Required output | Downstream consumer | Reopening or revision route |
|---|---|---|---|---|
| Pathway diagnosis | theory stack; transformation kernel | bounded finding, uncertainty, affected scope, lost response options | RPD design translation | new evidence returns to diagnosis |
| Design translation | transformation kernel | objective, testable requirement, alternatives, trade-off record | composition and RPE handoff | failed fit or changed assumption returns to design |
| Pattern composition | pattern language; composition rules | selected composition, conflicts, invariants, residual risks | evaluation and specification | failed invariant or interface returns to composition |
| Evaluation | evaluation protocol | stage-bounded finding with evidence class and limitations | design authority and assurance | counterevidence narrows or reopens claim |
| Specification and implementation | RPE handoff interface | specifications, implementation status, deviations, evidence mechanisms | assurance and operation | material deviation returns to named design authority |
| Assurance | assurance interface | bounded claim, evidence, assumptions, defeaters, uncertainty, review state | operational governance and human decision authority | trigger reopens claim, design, or operation state |
| Operational monitoring | monitoring and reopening protocol | signals, events, challenges, state transitions, residual-impact status | assurance and redesign authority | constrain, suspend, redesign, or retire through human authorization |
| Empirical research | empirical validation protocol; corpus protocol; coding manual | cases, observations, analyses, null/negative/rival/boundary/inconclusive findings | falsification and theory revision | retain, narrow, revise, suspend, or retire propositions through versioned review |

## Verification and evidence crosswalk

These are separate axes and must not be converted automatically or aggregated into a system-wide score.

| Axis | Values | Question answered | Does not establish |
|---|---|---|---|
| Evaluation stage | D / I / X / O / V | which object and stage was evaluated? | strength or independence of evidence by itself |
| Evidence class | E0–E5 | what kind of support is available? | that the evidence is relevant, sufficient, or unbiased |
| Assurance state | A0–A5 | how far a bounded claim package has progressed? | certification or whole-system quality |
| Empirical evidence level | V0–V5 | what research setting produced the evidence? | proof, universal validity, or causal effect |
| Corpus source tier | protocol-defined tier | what is the source and provenance condition? | comparability across contexts |
| Coding confidence | C0–C3 | how stable is a bounded coding decision? | pathway quality or desirability |

Reference interpretation of the evaluation stages:

| Stage | Bounded meaning |
|---|---|
| D | design traceability and coherence |
| I | implementation against specification |
| X | exercisability in controlled scenarios |
| O | observed operation in a stated period and context |
| V | broader contextual validation using relevant operational and independent or affected-party evidence |

## Responsibility-boundary table

| Function | Accountable role | Boundary |
|---|---|---|
| RPD design translation | named human or institutional design authority | does not implement, certify, or authorize itself |
| RPE specification and implementation | named implementation and operational owners | does not decide legal, social, or affected-party adequacy |
| Assurance review | named claim owner and independent reviewers where feasible | does not convert a bounded argument into certification |
| Operational state decision | authorized human or institution | owns continue, constrain, suspend, redesign, and retire decisions |
| Empirical analysis | named research owner under applicable governance | does not authorize deployment or erase adverse evidence |
| Theory revision | named maintainers and explicit human approval process | preserves dissent, version history, and unresolved evidence |

The exact placement of routine operation inside or outside RPE remains an unresolved theory-stack question. This table assigns functions without resolving that major conceptual choice.

## Terminology and namespace rules

| Term | Bounded definition | Qualified reference form |
|---|---|---|
| Claim | a scoped proposition owned by a named actor and limited by assumptions, evidence, defeaters, and time | `Claim <ID>` |
| Requirement | a testable response obligation with a performer and accountable human or institutional owner | `Requirement <ID>` |
| Evidence item | a versioned source or observation with scope, method, limitations, access, and provenance | `Evidence <ID>` |
| Counterevidence | evidence inconsistent with or limiting a proposition | `Counterevidence <ID>` |
| Defeater | a declared condition that can weaken, suspend, or defeat a claim or inference | `Defeater <ID>`; avoid unqualified `F*` |
| Reopening trigger | an event or threshold requiring reconsideration | `Trigger <ID>` |
| Reopening decision | a human-authorized state change after review | `Decision <ID>` |
| Kernel finding class | a transformation-kernel diagnosis category | `Kernel F1`–`Kernel F8` |
| Falsification class | a theory-revision challenge category | `Disconfirmation F*` or document-qualified ID |
| Assurance level | a claim-specific assurance state | `Assurance A0`–`A5` |
| Adjudication outcome | a coding-disagreement disposition | `AO-1`–`AO-7` in new records |

## Template coverage matrix

| Protocol requirement | Transformation | Composition / evaluation | Assurance | Empirical study | Observation log | Corpus manifest | Result report | Coding / operation extension |
|---|---|---|---|---|---|---|---|---|
| stable case and artifact identity | partial | partial | record / claim IDs | study ID | study, case, session, log IDs | case and linked artifact IDs | study, case, log, report IDs | coding and operation record IDs |
| finding → requirement → evidence trace | yes | yes | yes | yes | evidence references | source and code inventory | yes | source anchors |
| defeater and counterevidence | yes | yes | yes | yes | yes | finding table | yes | event and adjudication effects |
| uncertainty and minority interpretation | yes | yes | yes | yes | rival interpretation | corpus-level and linked record | yes | preserved coder rows and minority view |
| null / negative / rival-success | not primary | scenario counterevidence | counterevidence | explicit | observable | explicit | explicit | linked from case record |
| boundary / inconclusive | not primary | unknown / scope | unresolved claim | partial | uncertainty | explicit | unresolved scope | retained without forced consensus |
| residual ownership | yes | yes | yes | yes | yes | limitation fields | yes | operation event ledger |
| human authorization | yes | yes | yes | yes | authorization reference | release authorization | yes | adjudication / state-decision authorization |
| exclusion and withdrawal | not primary | not primary | not primary | withdrawal added | consent reference | exclusion, quarantine, withdrawal | limitations | coding status retained |
| periodic monitoring and reopening | handoff | reopening conditions | plan expanded | longitudinal design | events | longitudinal cases | result consequences | dedicated operation log |

## Navigation map

| Reader goal | Entry path |
|---|---|
| understand the theory | README → START-HERE → theory stack → kernel |
| design and evaluate | kernel → patterns / anti-patterns → composition → evaluation → templates |
| assure and operate | assurance interface → assurance record → monitoring protocol → operation log |
| run a study | empirical protocol → empirical study record → observation log → result report |
| build a case corpus | worked package → corpus protocol → coding manual → manifest → coding/adjudication record |
| challenge or revise theory | result report / corpus → falsification and theory revision → versioned human review |

## Human-gate questions

The following were deliberately not resolved in this audit:

1. Should the common stage vocabulary be D/I/X/O/V, and should the kernel's current operational-validation label be renamed?
2. May an explicit normative requirement enter RPD without an RPM finding, and what source-authority contract governs it?
3. Is routine operation inside RPE, outside it under operational governance, or represented as an interface spanning both?
4. Should existing identifier families be globally renamed, or only qualified in cross-document references?
5. Which Markdown-lint rules should become repository policy rather than ad hoc style findings?

These choices affect theory or repository-wide policy and require explicit human review before canonical adoption.
