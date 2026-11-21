# TER-002 — Dirt Terrain QA Plan

Status: DRAFT — no Dirt source files received yet  
Asset pack ID: `TER-002`  
Related specification: `docs/standards/TER-002-dirt-technical-spec.md`

## 1. QA objectives

Verify that every delivered Dirt source tile:
- conforms to the Vendrith 64 × 64 px terrain standard;
- is a valid, opaque PNG source asset;
- retains crisp HD top-down pixel-art rendering;
- tiles seamlessly in both axes;
- remains visually coherent with the other Dirt variants and the approved Grass terrain;
- has traceable metadata and an exact-source SHA-256 digest.

## 2. Required evidence per file

For each of the four planned files, record:

| Evidence | Required result |
|---|---|
| Filename and pack ID | Matches the technical specification |
| Image dimensions | Exactly 64 × 64 px |
| File format | Valid PNG |
| Color mode | Record actual mode; do not silently convert |
| Transparency | No transparent pixels; record alpha/channel information |
| File size | Record exact byte count |
| SHA-256 | Calculate from the delivered source binary |
| Native preview | Open and visually inspect the 64 × 64 source |
| 3 × 3 repeat preview | Shows nine exact repetitions of the source tile |
| Horizontal seam test | Right edge joins left edge without a visible discontinuity |
| Vertical seam test | Bottom edge joins top edge without a visible discontinuity |
| Visual review | Pixel clarity, palette, detail density, and style reviewed |
| Owner decision | Recorded separately from technical QA |

## 3. Seam and repeat tests

1. Build a 3 × 3 preview by repeating the exact source image; do not redraw or modify the source.
2. Inspect all horizontal and vertical joins at native scale and enlarged nearest-neighbor scale.
3. Inspect the four-tile junctions for obvious discontinuities or focal artifacts.
4. Run an edge-difference diagnostic and record the method and results. A non-zero edge difference is a diagnostic signal, not an automatic failure by itself; interpret it alongside the actual repeat preview.
5. Do not edit the source to make a diagnostic report pass without preserving the original and recording a new revision.

## 4. Visual acceptance checklist

- [ ] Correct top-down ground appearance.
- [ ] Pixel edges are crisp; no blur or unintended anti-aliasing.
- [ ] Palette and lighting are consistent with the Dirt set.
- [ ] Surface detail is restrained and readable at map scale.
- [ ] No distracting focal object or obvious repeated stamp.
- [ ] No text, border, grid, watermark, or preview overlay.
- [ ] No transparency or holes in the ground surface.
- [ ] No visible horizontal seam in the 3 × 3 preview.
- [ ] No visible vertical seam in the 3 × 3 preview.
- [ ] Tile junctions reviewed.
- [ ] Coherence with the approved Grass tile reviewed without modifying Grass.

## 5. Per-file status register

| File | Technical QA | Owner decision | Notes |
|---|---|---|---|
| `dirt_base.png` | NOT TESTED | NOT REVIEWED | Awaiting source |
| `dirt_dry.png` | NOT TESTED | NOT REVIEWED | Awaiting source |
| `dirt_dark.png` | NOT TESTED | NOT REVIEWED | Awaiting source |
| `dirt_texture.png` | NOT TESTED | NOT REVIEWED | Awaiting source |

Allowed technical QA outcomes: `PASS`, `CONDITIONAL PASS`, or `FAIL`. Owner decision must be a separate explicit record. Never infer owner approval from a technical pass.

## 6. Failure handling

- Preserve the delivered original binary and its initial checksum.
- Record each defect with the filename, test, observation, and evidence.
- Request a corrected source as a new revision; do not overwrite the original QA evidence.
- Re-run all applicable checks on the corrected source and calculate a new SHA-256.
- Do not commit a failed or unreviewed file as an approved production asset.

## 7. Final QA package

After testing, store the per-file results, source metadata, checksums, native previews, 3 × 3 previews, seam diagnostics, and owner decision under:

```text
docs/qa/terrain/TER-002/
```

The QA package must clearly distinguish source files from generated evidence. No result is implied until the actual files have been received and tested.
