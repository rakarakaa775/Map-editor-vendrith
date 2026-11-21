# VAL Evidence Supplement — VMA-GRASS-003 Source Package Verification

- **Record ID:** VAL-REG-EVIDENCE-002
- **Asset:** VMA-GRASS-003 / `grass_base.png`
- **Review date:** 2026-11-21
- **Review type:** Read-only package and checksum verification
- **Repository target:** `rakarakaa775/Map-editor-vendrith`, branch `main`
- **Scope:** Documentation only. No asset binary, editor code, map data, or license status changed.

## 1. Source package located

The project Library contains `VMA-GRASS-003.zip` (56,844 bytes). The archive was materialized for read-only inspection.

Archive SHA-256:
`6926873d679d35e419cff8ce3bf2aaeac4aec350de82326479fdd0a3b18f8477`

Archive members:
- `VMA-GRASS-003/ASSET_METADATA.txt` (652 bytes)
- `VMA-GRASS-003/SHA256SUMS.txt` (271 bytes)
- `VMA-GRASS-003/grass_base.png` (5,048 bytes)
- `VMA-GRASS-003/preview_3x3_native_192x192.png` (15,684 bytes)
- `VMA-GRASS-003/qa_preview_sheet_final.png` (46,015 bytes)

## 2. Original PNG checksum verification

The `grass_base.png` bytes were extracted from the archive in memory and hashed without editing or re-encoding.

- Actual byte length: **5,048**
- Actual SHA-256: `97682afaae999f282d06047b590d0725accb484c3c9735827a58291a8f573a32`
- Match against archive `SHA256SUMS.txt`: **MATCH**
- Match against `ASSET_METADATA.txt`: **MATCH**
- Match against the two previously supplied diagnostic reports: **MATCH**

This independently verifies the integrity of the PNG contained in the located VMA-GRASS-003 archive and confirms that its digest matches the reported digest.

## 3. Provenance evidence and limits

The package metadata records:
- Primary reference: `1795169202164.jpg`
- Secondary reference: `1795169265857.jpg`
- License status: `UNKNOWN`
- Repository integration: `NOT INTEGRATED`
- Approval status: `QA_PENDING`

**Important discrepancy:** the previously surfaced VMA-GRASS-002 production records refer to `1795169202164.jpg` and `1795169265857.jpg` in their own VMA-GRASS-002 context. They describe a Gemini-assisted workflow for VMA-GRASS-002, not direct creation evidence for VMA-GRASS-003. The shared reference filenames are contextual continuity only; they do not establish the complete VMA-GRASS-003 creation chain.

The exact file `input_file_36.png` was not present among the members of `VMA-GRASS-003.zip`, and no corresponding file was located in the Library metadata listing/search performed for this review. Therefore, the previously reported byte-for-byte copy relationship between `input_file_36.png` and `grass_base.png` remains **UNVERIFIED**. No claim is made that the source file was found or compared.

The archive itself contains no creator identity, generation transcript, prompt/session export, timestamped creation log, or explicit rights grant for the source references. The archive checksum and PNG checksum prove package/file integrity, not authorship, licensing, or commercial-use rights.

## 4. Updated evidence assessment

| Control | Result |
|---|---|
| VMA-GRASS-003 archive located | VERIFIED |
| Archive SHA-256 recorded | VERIFIED |
| PNG size and SHA-256 re-computed | VERIFIED |
| PNG digest matches package manifest and metadata | VERIFIED |
| Diagnostic-report digest consistency | VERIFIED |
| `input_file_36.png` source-chain comparison | NOT VERIFIED |
| Direct VMA-GRASS-003 creation record | NOT FOUND IN REVIEWED MATERIAL |
| Rights / license grant | NOT ESTABLISHED |
| Runtime QA | NOT TESTED |
| Asset binary repository integration | NOT INTEGRATED |

## 5. Registry decision

No status upgrade is authorized by this evidence supplement.

- **Provenance:** `PROVENANCE_PENDING_REVIEW`
- **License:** `LICENSE_PENDING_REVIEW` / `UNKNOWN`
- **Technical file integrity:** `VERIFIED` for the PNG contained in the located archive
- **Visual seam assessment:** retain the existing `CONDITIONAL PASS`; this supplement does not repeat or expand visual QA
- **Runtime QA:** `NOT TESTED`
- **Repository integration:** `NOT INTEGRATED`

## 6. Next evidence needed

To close provenance, the evidence set must include a directly attributable VMA-GRASS-003 creation/handover record or the exact claimed `input_file_36.png` source with a verifiable comparison and context linking it to this asset. To close licensing, the applicable rights terms for the original references and the generated/derived output must be established. Until then, do not mark the asset cleared for commercial use or change its license category from UNKNOWN.

---
**Audit posture:** read-only verification; no source pixels or project runtime files modified.
