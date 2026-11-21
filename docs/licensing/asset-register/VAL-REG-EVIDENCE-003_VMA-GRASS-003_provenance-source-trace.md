# VMA-GRASS-003 — Provenance Source-Trace Addendum

- **Record ID:** VAL-REG-EVIDENCE-003
- **Asset:** `VMA-GRASS-003` / `grass_base.png`
- **Review scope:** Library source-trace, metadata reconciliation, read-only
- **Repository:** `rakarakaa775/Map-editor-vendrith`, branch `main`
- **No binary, editor code, map data, or license status changed.**

## 1. Materials searched

The Library and conversation-file search was repeated for:
- `input_file_36.png`
- `1795169202164.jpg`
- `1795169265857.jpg` and `1795169265854.jpg`
- `0ac4c16e.jpeg`
- `41313696.jpeg`
- VMA-GRASS-003 creation / Gemini production / source handover records

The searches returned the VMA-GRASS-003 archive, its diagnostic reports, and VMA-GRASS-002 production PDFs. They did **not** return standalone binary records for `input_file_36.png`, either numbered reference image, `0ac4c16e.jpeg`, or `41313696.jpeg`, nor a direct VMA-GRASS-003 generation transcript. This is a statement about the accessible searched Library/conversation material, not proof that such records never existed elsewhere.

## 2. Exact metadata extracted from VMA-GRASS-003 archive

The archive's `ASSET_METADATA.txt` explicitly identifies:
- Task ID: `VMA-GRASS-003 (Source Asset Handover & Independent QA Preparation)`
- Primary reference: `1795169202164.jpg`
- Secondary reference: `1795169265854.jpg`
- License: `UNKNOWN`
- Repository integration: `NOT INTEGRATED`
- Approval: `QA_PENDING`

Its `SHA256SUMS.txt` lists the PNG digest already independently recomputed in Evidence Supplement 002. The archive therefore provides a source handover package and asset metadata, but it does not itself identify the creator, generation session, prompt, or legal rights in the reference images.

## 3. Cross-document discrepancy / attribution boundary

The VMA-GRASS-002 revision PDF and Gemini production directive describe an AI-assisted Gemini workflow for **VMA-GRASS-002**. Those documents identify the same primary reference filename, but they are not direct production records for VMA-GRASS-003.

The VMA-GRASS-003 archive independently repeats the reference filenames. This supports that the handover package associates those named references with VMA-GRASS-003, but does not prove the actual source image bytes, ownership, license terms, or the specific generation process used for VMA-GRASS-003.

The secondary reference is consistently `1795169265854.jpg` in the VMA-GRASS-003 archive and VMA-GRASS-002 technical revision. An earlier search query included `1795169265857.jpg`; no evidence was found for that alternate filename. Use `...5854.jpg` as the recorded filename and do not silently normalize it to `...5857.jpg`.

## 4. Provenance chain status

| Link | Evidence status |
|---|---|
| VMA-GRASS-003 handover archive exists in Library | VERIFIED |
| Archive metadata associates two named reference filenames | VERIFIED |
| Final PNG byte integrity and checksum | VERIFIED in Evidence Supplement 002 |
| Actual binary bytes for the two named reference images | NOT LOCATED |
| Actual binary bytes for `input_file_36.png` | NOT LOCATED |
| Byte-for-byte comparison between `input_file_36.png` and final PNG | NOT PERFORMED |
| Direct VMA-GRASS-003 prompt / generation transcript | NOT LOCATED |
| Creator identity / generation account attribution | NOT ESTABLISHED |
| Rights or license grant for source references and output | NOT ESTABLISHED |

## 5. Governance conclusion

The evidence supports a verified VMA-GRASS-003 handover package and verified final PNG integrity. It does not yet establish a complete creation/provenance chain or rights clearance.

Keep:
- `PROVENANCE_PENDING_REVIEW`
- `LICENSE_PENDING_REVIEW` / `UNKNOWN`
- Runtime QA: `NOT TESTED`
- Asset binary integration: `NOT INTEGRATED`

Do not infer VMA-GRASS-003 creation method from VMA-GRASS-002 records. Do not mark the asset commercially cleared. No additional repository action is authorized by this addendum.
