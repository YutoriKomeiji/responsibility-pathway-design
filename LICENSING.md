# RPD Licensing Scope

Responsibility Pathway Design (RPD) separates the license for design/research material from the license for software surfaces.

## Documentation, design, and research material — CC BY 4.0

Unless a file or directory explicitly states otherwise, the following are licensed under the Creative Commons Attribution 4.0 International License (CC BY 4.0):

- Markdown and prose documentation;
- design frameworks and pattern descriptions;
- diagrams and explanatory figures;
- templates and records intended as design/review artifacts;
- worked examples expressed as documentation or structured design material;
- research notes, terminology, and methodological text.

See `LICENSE` for the repository notice and the canonical CC BY 4.0 terms.

## Software and executable scripts — MIT

Software source code and executable scripts that are explicitly identified as software are licensed under the MIT License in `LICENSE-SOFTWARE-MIT`.

RPD is currently documentation/design-heavy. The separate MIT surface exists so that future executable helpers, validators, generators, or other software do not inherit a content-oriented Creative Commons license merely because they live in this repository.

When software is added, its file header, directory README, or adjacent notice should identify the MIT license where practical.

## Precedence

1. An explicit per-file license notice controls that file.
2. An explicit directory-level license notice controls files in that directory unless a file overrides it.
3. Otherwise, non-software material defaults to CC BY 4.0 under `LICENSE`.
4. Software explicitly identified as software defaults to MIT under `LICENSE-SOFTWARE-MIT`.

If a contribution mixes substantial software and expressive documentation in one artifact, contributors should split the artifact where practical or state the intended licensing boundary explicitly.

## Why this split exists

RPD's primary public output is a reusable design and research framework, for which CC BY 4.0 supports sharing, adaptation, critique, teaching, and derivative design work with attribution. Executable software has different reuse and integration expectations, for which MIT is the clearer fit.

This licensing split is about reuse terms. It does not change RPD's claim boundaries, evidence maturity, or responsibility boundaries.
