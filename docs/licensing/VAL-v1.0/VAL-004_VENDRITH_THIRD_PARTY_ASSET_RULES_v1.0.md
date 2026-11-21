# VENDRITH THIRD-PARTY ASSET RULES
## VAL-004 — Version 1.0

**Project:** Vendrith  
**Document ID:** VAL-004  
**Related policies:** VAL-001, VAL-002, and VAL-003  
**Status:** APPROVED — EFFECTIVE 2026-11-21  
**Effective date:** 2026-11-21

## 1. Purpose and scope

These rules govern the acquisition, review, modification, storage, attribution, and distribution of externally sourced materials used in Vendrith.

They apply to tilesets, terrain textures, sprites, audio, fonts, UI assets, 3D models, code, shaders, and other external materials.

## 2. Source identification

For each third-party asset, record the asset name and filename, creator/publisher, source URL or acquisition location, acquisition date if known, exact license name and version, license text or URL, attribution requirements, and known restrictions.

If the source cannot be verified, mark provenance `PROVENANCE_PENDING_REVIEW`.

## 3. License verification

Before approving a proposed use, review the applicable license and establish, where relevant:

- Commercial-use permission.
- Modification and derivative-work permission.
- Redistribution permission.
- Attribution and notice requirements.
- Share-alike or copyleft obligations.
- Source-file distribution requirements.
- Other conditions or restrictions.

A license name alone is insufficient if the exact terms or version cannot be established.

## 4. Preservation and priority

The original third-party license remains applicable to the external asset. VAL does not replace or override it.

Preserve required copyright notices, license text, attribution, source references, and other notices. Do not label third-party assets `VAL-ORIGINAL`.

## 5. Modification and derivatives

Modification does not automatically transfer ownership of the original asset to Vendrith.

Record the parent asset ID/version, original creator/source/license, modifications, responsible contributor, output filename and ID, output checksum, and applicable derivative restrictions. Confirm that the intended derivative use is compatible with the source license.

## 6. AI-assisted use of third-party materials

When external material is used as an AI reference or input, record its source and license, the input/reference used, AI tool, resulting output, modification workflow, and unresolved restrictions.

Using a third-party asset as an AI input does not automatically eliminate obligations under its original license. Review both the source terms and applicable AI platform terms.

## 7. Attribution

Where attribution is required, preserve the information specified by the source license. An attribution record should include asset title, creator, source URL, license name/version, required copyright notice, and modification statement where required.

Place attribution in the appropriate project credits, notices, or distribution materials.

## 8. Prohibited practices

Unless expressly permitted by the applicable license, do not:

- Redistribute third-party source assets independently.
- Remove copyright or attribution notices.
- Claim third-party assets as original Vendrith creations.
- Apply a conflicting license to the original asset.
- Circumvent license restrictions.
- Use assets with unknown rights in commercial releases.
- Assume that a free download permits commercial use.

## 9. Approval procedure

1. Identify the asset and exact source.
2. Locate and preserve the applicable license.
3. Verify license version and relevant terms.
4. Review commercial use, modification, and redistribution permissions.
5. Record attribution and restrictions.
6. Register provenance under VAL-002.
7. Register the asset under VAL-003.
8. Record the intended use and license decision.
9. Approve, restrict, or reject that intended use.

If a material licensing question remains unresolved, keep the asset pending review.

## 10. License conflicts

If a license conflicts with a proposed project use, suspend that use, preserve the evidence, document the conflict, and obtain appropriate permission or select an alternative. Record the resolution before approval.

## 11. Commercial release

Before commercial release, every included third-party asset must have a verified source, reviewed applicable terms, documented attribution, and confirmed compatibility with the intended distribution. Exclude assets with unresolved material restrictions until resolved.

## 12. Relationship to other VAL documents

- VAL-001 defines the overall licensing framework.
- VAL-002 defines provenance evidence requirements.
- VAL-003 maintains the central asset registry.
- VAL-004 governs third-party materials.

**Document status:** APPROVED — EFFECTIVE 2026-11-21  
**Repository integration:** NOT AUTHORIZED
