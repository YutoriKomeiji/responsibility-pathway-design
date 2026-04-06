# Start Here — Responsibility Pathway Design (RPD)

If you are new to this repository, start with this page.

Responsibility Pathway Design (RPD) is a framework for designing how responsibility:
- flows
- breaks
- returns
- is rebound
- is repaired
across AI-involved systems.

RPD is not another local execution technique.
It sits above prompt engineering, context engineering, harness engineering, and governance checklists as a higher-order design layer for responsibility continuity.

## Read This First

### 1. Core principles
Read:
- `docs/principles.md`

This explains the basic logic of RPD:
- responsibility is a pathway, not a point
- delegation without rebinding is a defect
- repair and rollback are part of responsibility
- records are part of the pathway

### 2. Layer model
Read:
- `docs/layer-model.md`

This explains where pathway breaks can occur across:
- intent
- decision
- execution
- interface
- model behavior
- records
- repair

### 3. Failure and repair examples
Read:
- `docs/failure-and-repair-examples.md`

This shows how pathway failures appear in practice and how repair, rollback, and rebinding can be designed.

### 4. Positioning above harness engineering
Read:
- `docs/positioning-above-harness-engineering.md`

This explains why RPD should be read as a layer above current AI execution discourse.

### 5. Terminology and nearby concepts
Read:
- `docs/terminology-and-nearby-concepts.md`

This clarifies how RPD differs from nearby labels such as:
- Responsibility Engineering
- Responsibility Architecture
- End-to-End Accountability Design
- Sociotechnical Governance
- AI Governance
- Human-in-the-loop

### 6. Operating questions
Read:
- `docs/operating-questions.md`

This turns the framework into a compact review lens for live systems.

## Recommended Reading Path
- New to RPD:
  1. `docs/principles.md`
  2. `docs/layer-model.md`
  3. `docs/positioning-above-harness-engineering.md`
- Designing or reviewing deployment:
  1. `docs/operating-questions.md`
  2. `docs/failure-and-repair-examples.md`
  3. `docs/layer-model.md`
- Comparing RPD with nearby concepts:
  1. `docs/terminology-and-nearby-concepts.md`
  2. `docs/positioning-above-harness-engineering.md`

## One-Sentence Summary
Responsibility Pathway Design is a higher-order design framework for governing how judgment, delegation, execution, interruption, repair, and organizational responsibility flow across AI-involved systems.
