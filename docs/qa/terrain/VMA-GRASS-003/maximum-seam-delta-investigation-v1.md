# Maximum Seam Delta Investigation Report v1.0 — VMA-GRASS-003

- **Asset ID:** `VMA-GRASS-003`
- **Version:** `1.0`
- **Source Asset:** `grass_base.png` (`64 × 64 px`, `PNG RGBA`, `5048` bytes)
- **Verified SHA-256:** `97682afaae999f282d06047b590d0725accb484c3c9735827a58291a8f573a32`
- **Technical investigation decision:** `CONDITIONAL PASS`

> Historical report: the original report recorded the asset as QA_PENDING pending owner review. The separate owner approval record in this directory supersedes that pending approval status without changing the historical investigation findings.

## 1. Exact Pixel Coordinates & RGB Values at Maximum Seam Deltas

### A. Horizontal Seam Maximum Delta (77 on Green Channel)

- Boundary transition: right edge column `x = 63` to left edge column `x = 0` at row `y = 25`.
- Pixel A — Right Edge (`x = 63, y = 25`): `RGB(8, 33, 11)`
- Pixel B — Left Edge (`x = 0, y = 25`): `RGB(34, 110, 38)`
- Signed delta (Pixel B − Pixel A): `ΔR = +26, ΔG = +77, ΔB = +27`
- Absolute delta: `|ΔR| = 26, |ΔG| = 77, |ΔB| = 27` (mean RGB delta: `43.33`)

### B. Vertical Seam Maximum Delta (101 on Green Channel)

- Boundary transition: bottom edge row `y = 63` to top edge row `y = 0` at column `x = 47`.
- Pixel A — Bottom Edge (`x = 47, y = 63`): `RGB(47, 134, 48)`
- Pixel B — Top Edge (`x = 47, y = 0`): `RGB(8, 33, 11)`
- Signed delta (Pixel B − Pixel A): `ΔR = −39, ΔG = −101, ΔB = −37`
- Absolute delta: `|ΔR| = 39, |ΔG| = 101, |ΔB| = 37` (mean RGB delta: `59.00`)

## 2. Comparison Against Interior RGB Delta Distribution

The tile uses a discrete 8-color pixel-art turf palette. Dark shadow greens and bright leaf highlights naturally produce large single-channel transitions.

| Metric | Horizontal interior (4,032 steps) | Vertical interior (4,032 steps) | Combined interior (8,064 steps) |
|---|---:|---:|---:|
| Max-channel delta mean | 25.52 | 24.66 | 25.09 |
| Max-channel delta standard deviation | 20.65 | 20.46 | 20.56 |
| Median / P90 / P99 | 20 / 54 / 85 | 20 / 54 / 85 | 20 / 54 / 85 |
| Interior maximum | 101 | 101 | 101 |
| Horizontal maximum percentile | 97.74% | — | 97.89% |
| Vertical maximum percentile | — | 100.00% | 100.00% |

Both boundary maxima occur within the upper tail of the interior single-channel delta distribution. The same high-contrast dark-to-bright blade clusters occur throughout the tile.

## 3. Root Cause & Visual Evaluation on 3 × 3 and 5 × 5 Grids

- Cause: local pixel-art blade/tuft contrast between adjacent dark-green and bright-green palette entries along the wrap boundary.
- The inspected pixels do not indicate a corrupted seam strip, alpha artifact, or unaligned color shift.
- At 3 × 3 (192 × 192 px) and 5 × 5 (320 × 320 px) repetition scales, neither point forms a noticeable break, line, or hotspot.
- General tile-period repetition remains recognizable on large uniform expanses and may be addressed later through deliberate variation, if needed.

## 4. Technical Decision

**CONDITIONAL PASS.** Neither maximum-delta pixel is considered a seam anomaly or visual defect. The condition concerns general repetition of a single tile over large uniform areas, not a seam failure.

The project owner approval is recorded separately in `OWNER-APPROVAL.md`.
