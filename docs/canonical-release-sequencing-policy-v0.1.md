# RPD Canonical Release Sequencing Policy v0.1

Status: Draft / Human Gate pending

## Purpose

This policy separates continuous public development from formal design-baseline release. Repository visibility, merge state, version tagging, and GitHub Release publication are distinct states.

## Current RPD state

RPD is a Public, continuously inspectable research and design repository. Public visibility allows external inspection of current and historical artifacts, but it does not declare every commit, branch, or merged pull request to be a formal design release.

## Canonical RPD artifact

A canonical RPD release is a specifically reviewed design baseline consisting of:

- an identified commit;
- a coherent document and template set;
- declared verification and validation vocabulary;
- traceability and boundary records;
- explicit limitations and reopening conditions;
- release metadata and citation information where applicable.

## Required sequence

1. define the intended release scope and version;
2. identify the candidate commit;
3. complete cross-document consistency, navigation, terminology, traceability, and boundary checks;
4. record successful, failed, unavailable, and deferred checks;
5. resolve or explicitly defer material findings;
6. obtain a Human Gate decision that the candidate is suitable as a bounded research baseline;
7. create the version tag only after that decision;
8. create a Draft GitHub Release and attach or reference the complete release-facing artifact set;
9. verify release notes, limitations, citation metadata, links, and correspondence to the tagged commit;
10. obtain a final Human Gate before publishing the GitHub Release or enabling immutable-release controls.

## Prohibited automatic transitions

The following must not occur automatically:

- merge to `main` → formal release;
- public repository update → version tag;
- pull-request approval → GitHub Release;
- GitHub Release publication → certification, standardization, or authorization to operate;
- RPD release → automatic RPE implementation release.

## Release-state vocabulary

| State | Meaning |
|---|---|
| public-working | inspectable ongoing research and design work |
| baseline-candidate | a bounded commit selected for release review |
| baseline-approved | Human Gate has approved the bounded design baseline |
| tagged | the approved commit has a version identifier |
| release-draft | release metadata and assets are staged but unpublished |
| released | GitHub Release has been explicitly published |
| reopened | new evidence or defects require review or revision of prior claims |

## Cross-layer boundary

An RPD release establishes only a reviewed design baseline within its declared scope. It does not prove RPE implementation conformity, operational effectiveness, external validation, certification, legal compliance, safety, or authorization to operate.

RPD may reference RPM findings and RPE implementation targets, but the exact source and target versions must be identified. A formal RPD release must not be treated as automatic evidence that the full RPM → RPD → RPE pathway is validated.

## Immutability rule

If immutable GitHub Releases are used, all intended release assets and metadata must be assembled and checked in Draft state before publication. An immutable public record must not be created before the canonical design-baseline review is complete.

## Human Gate

Release scope, version number, baseline approval, tag creation, release publication, immutability, citation metadata, and any standardization, certification, or operational claim remain human decisions.
