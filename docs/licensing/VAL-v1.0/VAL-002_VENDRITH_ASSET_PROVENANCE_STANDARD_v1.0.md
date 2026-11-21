# VENDRITH ASSET PROVENANCE STANDARD
## VAL-002 — Version 1.0

**Project:** Vendrith  
**Document ID:** VAL-002  
**Related policy:** VAL-001  
**Status:** APPROVED — EFFECTIVE 2026-11-21  
**Effective date:** 2026-11-21

## 1. Purpose and scope

This standard defines how Vendrith records the origin and history of digital assets, including terrain, sprites, UI, audio, fonts, models, and promotional materials.

Provenance means the documented history of an asset: its source, creator/provider, inputs, modifications, and supporting records.

## 2. Provenance categories

Use one primary category:

- `ORIGINAL_CREATION` — created by the project owner or an authorized contributor.
- `AI_GENERATED` — generated using a generative AI platform.
- `AI_ASSISTED_MODIFICATION` — derived from an existing source and modified using AI.
- `THIRD_PARTY_SOURCE` — acquired from an external creator, repository, marketplace, or provider.
- `UNKNOWN_ORIGIN` — origin cannot currently be established.

Do not classify an asset as original merely because its source is not known.

## 3. Evidence levels

| Level | Classification | Description |
|---|---|---|
| E0 | No evidence | No reliable origin evidence available |
| E1 | Informal evidence | Owner statement, recollection, or incomplete notes |
| E2 | Supporting evidence | Prompt records, screenshots, source references, or working files |
| E3 | Verifiable evidence | Original files, source records, license documents, and integrity checks |
| E4 | Complete provenance package | Consistent, traceable creation/acquisition history and relevant rights documentation |

Evidence level describes the available documentation; it is not a legal conclusion or proof of copyright ownership.

## 4. Required provenance record

Record the following fields where applicable:

| Field | Description |
|---|---|
| Asset ID / version | Exact project identifier and revision |
| Asset name / filename | Official name and binary filename |
| Provenance category | Category from Section 2 |
| Creator / provider | Known creator or source |
| Original source | URL, source file, repository, or platform |
| Creation/acquisition date | Exact date or `UNKNOWN` |
| Modification history | Changes and responsible contributor |
| Input references | Source/reference materials |
| AI tool and prompt | Tool and prompt reference, or `NOT_APPLICABLE` / `NOT_PROVIDED` |
| License evidence | License document, URL, or `UNKNOWN` |
| Evidence level | E0–E4 |
| Provenance status | Review state |
| SHA-256 | Checksum of the exact binary, if available |
| Evidence location | Reports, archives, and supporting records |

## 5. Provenance statuses

| Status | Meaning |
|---|---|
| `PROVENANCE_PENDING_REVIEW` | Evidence has not yet been reviewed |
| `PROVENANCE_INCOMPLETE` | Material information is missing |
| `PROVENANCE_REVIEW_REQUIRED` | Evidence needs further investigation |
| `PROVENANCE_VERIFIED` | Available provenance evidence has been reviewed and accepted for the recorded purpose |
| `PROVENANCE_REJECTED` | Evidence is insufficient or inconsistent for the intended use |

`PROVENANCE_VERIFIED` does not by itself mean the asset is license-approved or commercially cleared. License review is separate under VAL-001.

## 6. Binary integrity and preservation

A read-only provenance audit may inspect file format, dimensions, size, metadata, and SHA-256; compare copies; and verify archive contents.

A read-only audit must not re-encode, resize, crop, recolor, recompress, or otherwise alter source binaries. Any intentional modification must be documented as a separate derivative or revision with its own identity and checksum.

A matching checksum demonstrates binary identity, not ownership or licensing rights.

## 7. Derivative asset tracking

For every derivative, record its parent asset ID and version, source license, relationship, modifications, contributor, output version, and output checksum.

A derivative does not automatically inherit unrestricted rights from its parent. Review the source license and derivative-work conditions before approving use.

## 8. AI platform records

Where available, retain the platform/tool name, applicable terms and review date, prompt, reference inputs, output, human post-processing, and known restrictions. Platform terms may change; identify the applicable version or date when possible.

Do not treat a prompt, generation receipt, or AI output alone as proof of exclusive ownership.

## 9. Review procedure

1. Identify the exact asset and version.
2. Record known origin and source.
3. Identify parent assets and external references.
4. Collect available creation/acquisition and license evidence.
5. Verify binary identity and integrity without modifying the source.
6. Identify missing or conflicting information.
7. Assign an evidence level and provenance status.
8. Record reviewer, date, decision, and evidence location.
9. Update the VAL Asset Registry.

Distinguish verified facts, owner statements, and assumptions.

## 10. Change control

Do not silently overwrite provenance history. Record the date, asset/version, field changed, previous and new values, reason, reviewer, and supporting evidence.

## 11. Relationship to other VAL documents

- VAL-001 governs license classification and permitted use.
- VAL-002 governs provenance evidence.
- VAL-003 maintains the asset registry.
- VAL-004 adds rules for third-party assets.

**Document status:** APPROVED — EFFECTIVE 2026-11-21  
**Repository integration:** NOT AUTHORIZED
