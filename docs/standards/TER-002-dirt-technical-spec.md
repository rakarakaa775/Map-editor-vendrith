# TER-002 — Dirt Terrain Technical Specification

Status: DRAFT — documentation only  
Asset pack ID: `TER-002`  
Repository: `rakarakaa775/Map-editor-vendrith`  
Target directory: `assets/terrain/dirt/`

## 1. Purpose

Define the production requirements for the first Vendrith dirt-ground terrain set. This document is a production brief; it does not mean that any Dirt PNG has been created, accepted, or committed.

## 2. Applicable project standard

All source tiles must follow `docs/standards/terrain-asset-standard.md`:

- Native source size: 64 × 64 pixels.
- PNG format.
- HD top-down pixel-art style.
- No baked-in labels, borders, registration marks, or preview overlays.
- Keep source tiles separate from previews, contact sheets, and diagnostic images.
- Preserve the exact source binary after acceptance; revisions require a new version and QA record.

The tile is intended for top-down orthographic map use. Any 2:1 source-to-logical-cell scaling must use nearest-neighbor sampling in the consuming renderer.

## 3. Planned source files

The pack plans four distinct ground tiles. Produce and review the base tile first; the remaining variants are planned members of the same pack and must not be treated as approved merely because the base tile passes.

| Planned file | Role | Visual direction |
|---|---|---|
| `dirt_base.png` | Primary natural soil ground | Balanced medium-brown earth, subtle granular detail, restrained small stones/soil variation |
| `dirt_dry.png` | Dry soil variation | Lighter, warmer and drier earth; sparse fine cracks only, not large distracting fissures |
| `dirt_dark.png` | Dark/moist soil variation | Deeper brown earth with restrained damp tonal variation; no glossy water-like highlights |
| `dirt_texture.png` | Alternate soil surface variation | Distinct but compatible granular/earthy pattern to reduce visible repetition |

All four are independent, repeatable ground tiles. They must share a coherent palette, pixel scale, lighting direction, detail density, and overall rendering style. Variants must be distinguishable at normal map zoom without looking like unrelated art styles.

## 4. Visual and technical constraints

- Exact canvas: 64 × 64 pixels per source file.
- PNG; opaque ground surface (no transparent holes or transparent background).
- Top-down / orthographic presentation; no perspective horizon or side-facing view.
- Pixel-art clusters must remain crisp. Do not apply blur, anti-aliasing, smooth gradients, or resampling that softens pixel edges.
- Use controlled tonal clusters and restrained detail. Avoid noisy single-pixel scatter, excessive contrast, large isolated focal objects, text, symbols, footprints, plants, grass tufts, paths, or props.
- No visible border, frame, shadow around the tile, or baked-in grid.
- The left/right and top/bottom edges must repeat cleanly. Edge pixels and clusters must be designed for tiling, not merely hidden by a preview.
- No external/legacy LPC assets. Create original Vendrith artwork only.

## 5. Production order

1. Create `dirt_base.png` first.
2. Submit its native PNG and preview evidence for technical review.
3. Resolve any visual or seam defects before creating the remaining variants.
4. Create `dirt_dry.png`, `dirt_dark.png`, and `dirt_texture.png` as a coordinated set.
5. QA and approve each source file independently.

Do not generate all variants by recoloring or mechanically transforming one tile unless the owner explicitly approves that method. Each file must be visually reviewed as its own source asset.

## 6. Required delivery structure

```text
assets/terrain/dirt/
├── dirt_base.png
├── dirt_dry.png
├── dirt_dark.png
├── dirt_texture.png
├── README.md
└── previews/
    ├── preview_3x3_dirt_base.png
    ├── preview_3x3_dirt_dry.png
    ├── preview_3x3_dirt_dark.png
    └── preview_3x3_dirt_texture.png
```

Keep QA reports under `docs/qa/terrain/TER-002/`. Previews are evidence only and must never be substituted for source PNGs.

## 7. Acceptance boundary

This specification does not grant asset approval. Each file remains `PENDING` until its native binary, metadata, checksum, visual review, seam tests, and owner decision are recorded. Do not update the Grass asset or its historical QA records as part of Dirt production.
