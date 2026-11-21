# VAL Registry Evidence Index — VMA-GRASS-003

**Record ID:** VAL-REG-INDEX-004  
**Asset ID:** VMA-GRASS-003  
**Repository:** `rakarakaa775/Map-editor-vendrith`  
**Branch:** `main`  
**Review date:** 2026-11-22  
**Record type:** Documentation-only evidence index  
**Asset binary modified:** No  
**Editor/map data modified:** No

## 1. Purpose

This index connects the provisional VMA-GRASS-003 entry in VAL-003 with the audit records currently available in the repository. It is an evidence-navigation record only; it does not replace VAL-003, establish copyright ownership, grant a license, or authorize repository integration or distribution.

## 2. Evidence records

| Evidence ID | Repository path | What it establishes |
|---|---|---|
| VAL-REG-AUDIT-001 | `docs/licensing/asset-register/VAL-REG-AUDIT-001_VMA-GRASS-003_preliminary.md` | Preliminary technical/visual audit findings and provisional status. |
| VAL-REG-EVIDENCE-002 | `docs/licensing/asset-register/VAL-REG-EVIDENCE-002_VMA-GRASS-003_source-package-verification.md` | Independent SHA-256 verification of the PNG contained in the supplied VMA-GRASS-003 ZIP and archive manifest consistency. |
| VAL-REG-EVIDENCE-003 | `docs/licensing/asset-register/VAL-REG-EVIDENCE-003_VMA-GRASS-003_provenance-source-trace.md` | Source-trace findings, metadata reference filenames, and limitations of the currently available provenance evidence. |

## 3. Verified binary identity

The `grass_base.png` file extracted from the VMA-GRASS-003 source archive was independently hashed and matched the archive's checksum manifest:

- Filename: `grass_base.png`
- Dimensions / format: 64 × 64 PNG RGBA
- File size: 5,048 bytes
- SHA-256: `97682afaae999f282d06047b590d0725accb484c3c9735827a58291a8f573a32`
- Source archive SHA-256: `6926873d679d35e419cff8ce3bf2aaeac4aec350de82326479fdd0a3b18f8477`

This confirms the integrity and identity of the PNG bytes in the inspected archive. It does not establish who created the image, ownership of underlying rights, the license applicable to it, or whether the named reference images were actually used.

## 4. Provenance evidence boundary

The archive metadata names these references:

- Primary reference: `1795169202164.jpg`
- Secondary reference: `1795169265854.jpg`

The inspected archive contains metadata naming these files, but the reference-image binaries and a direct VMA-GRASS-003 creation/generation transcript were not located in the searched Library/conversation materials. The metadata association alone is not proof of source-image contents, creator identity, rights ownership, or generation history.

A separate VMA-GRASS-002 production directive or report must not be treated as direct creation evidence for VMA-GRASS-003.

## 5. Current independent status dimensions

| Dimension | Current status | Basis |
|---|---|---|
| PNG integrity | VERIFIED | Independent hash of archive PNG matches archive manifest. |
| Source handover archive | VERIFIED | Archive contents and archive checksum inspected. |
| Provenance | PROVENANCE_PENDING_REVIEW | Direct source binaries and creation/rights evidence remain incomplete. |
| License | UNKNOWN / LICENSE_PENDING_REVIEW | No applicable license or permission evidence established. |
| Visual / technical QA | PASS_WITH_CAVEATS (reported) | Refer to preliminary audit; this index does not re-run the tests. |
| Runtime QA | NOT_TESTED | No runtime result recorded. |
| Owner approval | Conditional visual approval reported only | No license or commercial approval inferred. |
| Repository asset integration | NOT_INTEGRATED | No asset binary integration performed. |
| Commercial clearance | NOT ESTABLISHED | Rights and permissions remain unresolved. |

## 6. Required next evidence

To close provenance and license review, obtain and verify the original reference-image files, direct VMA-GRASS-003 creation/generation or handover records, creator/provider identity, and applicable license or explicit permission covering the intended use. Record each item against the exact asset revision before changing any status.

## 7. Change history

| Date | Change | Previous state | New state |
|---|---|---|---|
| 2026-11-22 | Added an evidence-navigation index linking the existing audit, binary verification, and provenance trace records. | Evidence records existed independently. | Evidence records cross-referenced; all substantive asset statuses unchanged. |

**Disposition:** DOCUMENTATION-ONLY INDEX RECORDED  
**Asset license:** PENDING REVIEW  
**Asset provenance:** PENDING REVIEW  
**Asset binary integration:** NOT AUTHORIZED BY THIS RECORD
