# VAL Asset Registration & Provenance Audit — VMA-GRASS-003

**Audit record:** VAL-REG-AUDIT-001  
**Asset:** VMA-GRASS-003  
**Revision:** 1.0  
**Audit date:** 2026-11-21  
**Audit mode:** Documentation-led, read-only preliminary review  
**Audit status:** PRELIMINARY — EVIDENCE GAPS OPEN  
**Asset status:** QA_PENDING (unchanged)  
**License status:** LICENSE_PENDING_REVIEW (unchanged)  
**Provenance status:** PROVENANCE_PENDING_REVIEW (unchanged)  
**Repository integration of asset binary:** NOT AUTHORIZED

## 1. Purpose

This is the first asset registration and provenance audit performed under VAL v1.0. The initial subject is VMA-GRASS-003 (`grass_base.png`). This record consolidates available project reports without modifying or copying the source PNG.

This is not a legal opinion, a fresh binary examination, or a declaration of commercial clearance.

## 2. Evidence reviewed

The following Library records were located and reviewed at the documentation/snippet level:

1. `grass_seam_diagnostic_report_v1.md`
2. `grass_max_delta_investigation_report_v1.md` (including the duplicate `(1)` copy)
3. `Vendrith Terrain Pack v1.1 - Grass Prototype Technical Revision (VMA-GRASS-002-REVISION).pdf`
4. `GEMINI PRODUCTION DIRECTIVE--VENDRITH GRASS PROTOT....pdf`

The VMA-GRASS-002 documents describe an earlier prototype/revision and are contextual evidence only. They must not be treated as direct proof of the origin of VMA-GRASS-003.

## 3. Identity and technical facts reported for VMA-GRASS-003

| Field | Recorded value | Evidence status |
|---|---|---|
| Asset ID | VMA-GRASS-003 | Reported in diagnostic records |
| Version | 1.0 | Reported in diagnostic records |
| Filename | `grass_base.png` | Reported |
| Dimensions | 64 × 64 px | Reported |
| Format / mode | PNG / RGBA | Reported |
| File size | 5,048 bytes | Reported |
| SHA-256 | `97682afaae999f282d06047b590d0725accb484c3c9735827a58291a8f573a32` | Reported by two diagnostic records |
| Logical cell size | 32 × 32 px | Project specification context |
| Unique palette colors | 8 | Reported by seam diagnostic |
| Asset status | QA_PENDING | Reported; retained |

**Important:** The checksum is transcribed from the existing diagnostic reports. The exact source PNG bytes were not independently re-hashed during this preliminary audit. Therefore the digest is a reported value, not a new verification result from this audit.

## 4. Technical QA evidence — separate from provenance and licensing

The seam diagnostic reports:
- Horizontal seam mean RGB delta: 15.5729; interior adjacent-column baseline: 14.6415.
- Vertical seam mean RGB delta: 15.9896; interior adjacent-row baseline: 14.8327.
- Horizontal and vertical maximum single-channel deltas: 77 and 101 respectively.
- Diagnostic conclusion: CONDITIONAL PASS, with no solid seam line reported.

The maximum-delta investigation explains the outlier pixels as transitions between dark shadow greens and brighter leaf-highlight greens in an eight-color palette. Its conclusion is also CONDITIONAL PASS.

These reports support a conditional technical/visual finding only. They do not establish provenance, license permission, runtime behavior, owner approval, or repository integration.

## 5. Provenance assessment under VAL-002

| Required field | Current finding |
|---|---|
| Provenance category | UNKNOWN_ORIGIN pending direct source-chain confirmation |
| Creator / provider | NOT ESTABLISHED by the reviewed VMA-GRASS-003 reports |
| Original source / source URL | NOT ESTABLISHED |
| Creation or acquisition date | NOT ESTABLISHED for VMA-GRASS-003 |
| Creation method / tool | NOT ESTABLISHED for VMA-GRASS-003 |
| Prompt and reference inputs | NOT ESTABLISHED for VMA-GRASS-003 |
| Modification history | Existing reports describe read-only diagnostics; complete creation/edit history not established |
| Parent asset / derivative relationship | NOT ESTABLISHED |
| Evidence level | E1 — limited documentary evidence; source chain incomplete |
| Provenance status | PROVENANCE_PENDING_REVIEW |

The earlier VMA-GRASS-002 production directive describes Gemini-assisted creation and references Candidate A/B and source raster files. Because it identifies VMA-GRASS-002, that information cannot be automatically assigned to VMA-GRASS-003. A relationship between these assets must be demonstrated, not assumed.

The prior project record that a binary copy was preserved byte-for-byte from `input_file_36.png` is useful as a reported chain-of-custody statement, but the original file and transfer record must be directly inspected before it can establish the complete origin of the asset.

## 6. License assessment under VAL-001

**License category:** UNKNOWN  
**License status:** LICENSE_PENDING_REVIEW  
**Commercial clearance:** NOT ESTABLISHED

No direct VMA-GRASS-003 license grant, applicable AI platform terms, third-party source license, or complete creator-rights record was established in the reviewed material. A verified checksum and successful QA do not establish usage rights.

## 7. Registration entry — preliminary

| Registry field | Value |
|---|---|
| Asset ID / version | VMA-GRASS-003 / 1.0 |
| Name / filename | Grass Base / `grass_base.png` |
| Category | Terrain — grass base tile |
| Dimensions / format | 64 × 64 px / PNG RGBA (reported) |
| Provenance category | UNKNOWN_ORIGIN |
| Provenance evidence level | E1 — preliminary |
| Provenance status | PROVENANCE_PENDING_REVIEW |
| License category / status | UNKNOWN / LICENSE_PENDING_REVIEW |
| SHA-256 | `97682afaae999f282d06047b590d0725accb484c3c9735827a58291a8f573a32` (reported; not re-hashed in this audit) |
| Visual / technical QA | CONDITIONAL PASS reported by diagnostic documents |
| Runtime QA | NOT TESTED |
| Owner approval | Not established by the reviewed evidence |
| Asset binary repository status | NOT_INTEGRATED |
| Restrictions | No commercial clearance; no license upgrade |

## 8. Open evidence requirements

The following items are required before provenance can advance beyond preliminary review:

1. Inspect the exact original `grass_base.png` binary and recompute SHA-256 directly.
2. Inspect `input_file_36.png` and its source/transfer context; verify whether it is byte-identical to the registered binary.
3. Establish who created the source artwork and when, distinguishing the original artwork from later pixel conversion or reconstruction.
4. Identify any AI platform, prompt, reference images, and applicable terms specifically for VMA-GRASS-003, if used.
5. Establish whether VMA-GRASS-003 is original, a derivative of VMA-GRASS-002, or an independently created asset.
6. Locate the applicable license/terms and record attribution or restrictions.
7. Preserve evidence locations and reviewer/date for each verified fact.

No missing field may be filled by inference from the similar filename `grass_base.png` or from VMA-GRASS-002 records.

## 9. Audit conclusion

**Preliminary registration completed; provenance and license review remain OPEN.**

VMA-GRASS-003 has enough documentary technical information for a preliminary registry entry, but not enough direct source-chain or rights evidence to classify it as VAL-ORIGINAL, VAL-AI-ASSISTED, or VAL-THIRD-PARTY with confidence.

The correct current states remain:

- `PROVENANCE_PENDING_REVIEW`
- `LICENSE_PENDING_REVIEW`
- `QA_PENDING` (existing asset governance state retained)
- Runtime QA: `NOT_TESTED`
- Commercial clearance: `NOT ESTABLISHED`

No source binary, PNG, editor code, map data, or individual asset license status was changed by this audit.

## 10. Next action

Continue with direct inspection of the exact VMA-GRASS-003 source binary and its `input_file_36.png` chain-of-custody evidence. Do not upgrade provenance or license status until those records and applicable rights evidence are verified.
