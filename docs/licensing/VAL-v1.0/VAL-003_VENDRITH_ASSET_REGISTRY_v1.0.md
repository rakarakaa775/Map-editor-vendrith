# VENDRITH ASSET REGISTRY
## VAL-003 — Version 1.0

**Project:** Vendrith  
**Document ID:** VAL-003  
**Related policies:** VAL-001 and VAL-002  
**Status:** APPROVED — EFFECTIVE 2026-11-21  
**Effective date:** 2026-11-21

## 1. Purpose

The Vendrith Asset Registry is the central inventory for tracking asset identity, provenance, integrity, QA, licensing, restrictions, and repository integration.

It is an administrative record. It does not independently establish copyright ownership or grant usage rights.

## 2. Asset identification

Use a unique, stable Asset ID. Existing identifiers must not be changed merely to fit a naming convention; corrections require a documented decision.

Example identifiers include `VMA-GRASS-003`, `TER-002`, `TER-003`, and `TER-004`. Preserve the project's established identifiers and distinguish asset IDs from filenames and revision labels.

## 3. Registry fields

Each record should include:

| Field | Description |
|---|---|
| Asset ID / version | Stable identifier and exact revision |
| Asset name / filename | Official name and source filename |
| Category | Terrain, character, UI, audio, etc. |
| Dimensions / format | Applicable technical properties |
| Creator / provider | Known creator or source |
| Provenance category | VAL-002 category |
| Evidence level / status | VAL-002 review result |
| License category / status | VAL-001 classification and review result |
| SHA-256 | Checksum for the exact binary |
| Visual QA | Visual review status |
| Technical QA | Static/technical verification status |
| Runtime QA | In-engine verification status |
| Owner approval | Explicit owner decision, if any |
| Repository status | Integration state |
| Restrictions | Known limitations |
| Evidence location | Reports, archives, source records |
| Last reviewed | Date of latest review |

Unknown information must be marked `UNKNOWN` or `NOT_PROVIDED`.

## 4. Independent status dimensions

### 4.1 Visual QA
`NOT_TESTED`, `PENDING_REVIEW`, `PASS`, `PASS_WITH_CAVEATS`, `FAIL`

### 4.2 Technical QA
`NOT_TESTED`, `PENDING_REVIEW`, `PASS`, `PASS_WITH_CAVEATS`, `FAIL`

### 4.3 Runtime QA
`NOT_TESTED`, `PENDING`, `PASS`, `PASS_WITH_CAVEATS`, `FAIL`

### 4.4 Provenance
Use the statuses defined in VAL-002.

### 4.5 License
Use the statuses defined in VAL-001.

### 4.6 Owner approval
Use explicit recorded decisions such as `PENDING_OWNER_REVIEW`, `APPROVED_WITH_CAVEATS`, `APPROVED`, or `REJECTED`. Do not infer approval from QA results.

### 4.7 Repository integration
`NOT_INTEGRATED`, `CANDIDATE`, `APPROVED_FOR_INTEGRATION`, `INTEGRATED`, `INTEGRATION_REJECTED`

Only mark an asset `INTEGRATED` when repository evidence confirms the exact integrated revision.

## 5. Initial terrain records — provisional snapshot

The entries below reflect project decisions and audit information reported to date. They are provisional administrative records, not a fresh binary, provenance, or license audit. Confirm exact revision and evidence before relying on any record for release.

### 5.1 VMA-GRASS-003 — Grass Base

| Field | Current record |
|---|---|
| Asset ID | VMA-GRASS-003 |
| Filename | `grass_base.png` |
| Dimensions / format | 64 × 64, PNG RGBA (reported) |
| SHA-256 | `97682afaae999f282d06047b590d0725accb484c3c9735827a58291a8f573a32` |
| Provenance category | `UNKNOWN_ORIGIN` |
| Provenance status | `PROVENANCE_PENDING_REVIEW` |
| License category | `UNKNOWN` |
| License status | `LICENSE_PENDING_REVIEW` |
| Visual QA | `PASS_WITH_CAVEATS` (reported conditional approval) |
| Technical QA | `PASS_WITH_CAVEATS` (reported conditional pass) |
| Runtime QA | `NOT_TESTED` |
| Owner approval | Conditional visual approval reported |
| Repository status | `NOT_INTEGRATED` |
| Restriction | No commercial clearance established |

### 5.2 TER-002 — Dirt Base V2

| Field | Current record |
|---|---|
| Asset ID | TER-002 |
| Purpose | Walkable dirt-ground surface candidate |
| Provenance category / status | `UNKNOWN` / `PROVENANCE_PENDING_REVIEW` |
| License category / status | `UNKNOWN` / `LICENSE_PENDING_REVIEW` |
| Visual QA | `PENDING_REVIEW` in this registry snapshot |
| Technical QA | Static compatibility checks reported as pass |
| Runtime QA | `NOT_TESTED` |
| Owner approval | Not recorded here |
| Repository status | `NOT_INTEGRATED` |
| Restriction | Runtime collision and autotile behavior unverified |

### 5.3 TER-003 — Dirt Cliff Face V4

| Field | Current record |
|---|---|
| Asset ID | TER-003 |
| Purpose | Non-walkable vertical dirt cliff face |
| Provenance category / status | `UNKNOWN` / `PROVENANCE_PENDING_REVIEW` |
| License category / status | `UNKNOWN` / `LICENSE_PENDING_REVIEW` |
| Visual QA | `PENDING_REVIEW` in this registry snapshot |
| Technical QA | Static compatibility checks reported as pass |
| Runtime QA | `NOT_TESTED` |
| Owner approval | Not recorded here |
| Repository status | `NOT_INTEGRATED` |
| Restriction | Runtime collision, lighting, and occlusion unverified |

### 5.4 TER-004 — Grass Edge / Cliff Top Transition

| Field | Current record |
|---|---|
| Asset ID | TER-004 |
| Version | 1.0 |
| Purpose | Grass cliff-top transition |
| Provenance category / status | `UNKNOWN` / `PROVENANCE_PENDING_REVIEW` |
| License category / status | `UNKNOWN` / `LICENSE_PENDING_REVIEW` |
| Visual QA | `APPROVED_WITH_CAVEATS` (owner approval reported) |
| Technical QA | `PASS_WITH_CAVEATS` (audit result reported) |
| Runtime QA | `NOT_TESTED` |
| Owner approval | `APPROVED_WITH_CAVEATS` |
| Repository status | `NOT_INTEGRATED` |
| Restrictions | Avoid identical variants consecutively; tonal seams reported at 4× zoom in specified arrangements |

## 6. Evidence rules

Every status change must be supported by evidence tied to the exact asset revision. Evidence may include original files, checksum manifests, technical reports, visual reports, runtime test results, license documents, creator records, and repository references.

A report for one revision must not automatically be applied to a later revision. Record whether evidence was directly inspected or reported by the owner; do not imply a fresh verification when none occurred.

## 7. Update and audit history

For each registry change, record date, Asset ID/version, field changed, previous value, new value, reason, supporting evidence, and reviewer/approver. Preserve relevant prior values.

## 8. Distribution gate

Visual or technical QA does not establish license approval. Runtime QA does not establish provenance. Repository integration does not establish commercial clearance.

Before commercial distribution, establish acceptable provenance, applicable permissions, third-party compatibility, attribution, and resolution of material restrictions. Assets with unresolved rights issues must not be treated as commercially cleared.

## 9. Version history

| Version | Change | Status |
|---|---|---|
| 1.0 | Initial provisional terrain registry | Approved — effective 2026-11-21 |

**Document status:** APPROVED — EFFECTIVE 2026-11-21  
**Repository integration:** NOT AUTHORIZED
