# Vendrith Terrain Asset Standard

Status: initial baseline  
Applies to: Vendrith Map Asset Pack

## Source asset requirements

- Native tile artwork: 64 × 64 pixels.
- Format: PNG; preserve the verified source bytes.
- Style: HD top-down pixel art.
- No baked-in labels, borders, registration marks, or preview overlays.
- Keep the source tile separate from previews, contact sheets, and diagnostic images.

## Production and acceptance

1. Assign a unique asset ID before QA.
2. Record dimensions, PNG mode, file size, and SHA-256 from the exact source binary.
3. Run visual review and applicable seam/tiling checks.
4. Preserve QA reports as historical evidence.
5. Record owner approval separately from the technical QA result.
6. Do not modify an approved source asset in place. Any revision receives a new version and a new QA record.

## Scope control

- Add only assets created specifically for Vendrith.
- Do not import legacy LPC assets until a separate decision is made after the Map Editor is complete.
- Avoid speculative variants. Produce additional assets only when a concrete Map Editor or map-content requirement exists.

## Logical rendering scale

The 64 × 64 px source tile may be rendered at a 32 × 32 px logical cell where the consuming renderer requires a 2:1 source-to-cell scale. This repository scaffold does not implement that renderer.
