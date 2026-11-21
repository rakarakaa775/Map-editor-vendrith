# Vendrith Map Editor

A dedicated workspace for the future Vendrith Map Editor and its approved, project-produced map assets.

## Current scope

This repository is an organized foundation only. It does not yet contain an implemented editor, rendering engine, deployment configuration, or integration with World of Vendrith.

### Asset policy

- Keep the asset library intentionally small.
- Add only assets produced specifically for Vendrith and approved by the project owner.
- Current source-art target: 64 × 64 px PNG, HD top-down pixel art.
- Do not import the legacy LPC asset collection at this stage.
- Preserve source files and record SHA-256 checksums for approved assets.

## Repository layout

- `assets/terrain/` — approved terrain source assets.
- `docs/standards/` — asset and production standards.
- `docs/asset-register/` — concise inventory and approval status.
- `docs/qa/` — technical QA reports and owner decisions.
- `editor/` — reserved for future Map Editor implementation.
- `map-data/` — reserved for future map data and schemas.
- `tools/validation/` — reserved for future asset validation tools.

## Current asset

The first reviewed asset is `VMA-GRASS-003` (`grass_base.png`). Its seam investigation received a CONDITIONAL PASS and the project owner approved it with the condition that large-area texture repetition remains a future variation consideration.

The binary PNG is not included in this initial scaffold because the source binary was not available in the files accessible for this repository operation. Its recorded checksum and technical details are preserved in the asset register and QA report. Add the exact original binary only after it is supplied; do not recreate or re-encode it.

## Project status

**Foundation only — implementation intentionally deferred.**
