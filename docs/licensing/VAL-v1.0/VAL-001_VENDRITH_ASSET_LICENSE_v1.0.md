# VENDRITH ASSET LICENSE (VAL)
## Version 1.0 — Approved and Effective 2026-11-21

**Project:** Vendrith  
**Document ID:** VAL-001  
**Version:** 1.0  
**Status:** APPROVED — EFFECTIVE 2026-11-21  
**Effective date:** 2026-11-21  
**Scope:** Digital assets used in the Vendrith project

## 1. Purpose

The Vendrith Asset License (VAL) establishes an internal framework for classifying, documenting, reviewing, and managing assets used in Vendrith. It helps the project track provenance, applicable permissions, attribution, restrictions, and distribution readiness.

VAL is a project policy. It does not create copyright, guarantee exclusive ownership, replace third-party licenses, or grant rights that the project owner or contributors do not otherwise possess.

## 2. License categories

Each asset must be assigned one primary category after review.

### 2.1 `VAL-ORIGINAL`
For assets created by the project owner or an authorized contributor, where the relevant creation history and rights are sufficiently documented.

Record the creator, source files where available, creation history, contributors, and any external inputs.

### 2.2 `VAL-AI-ASSISTED`
For assets generated or substantially modified using generative AI tools.

Record the platform, available prompts and inputs, generation or modification workflow, human edits, applicable platform terms, and any third-party materials. This category does not guarantee copyright protection, exclusivity, or unrestricted commercial use.

### 2.3 `VAL-THIRD-PARTY`
For assets obtained from external creators, repositories, marketplaces, or providers.

The original license remains applicable. Record the source, creator, exact license and version, required attribution, and restrictions. VAL does not replace or override that license.

An asset with insufficient evidence must remain `UNKNOWN` or `LICENSE_PENDING_REVIEW`; do not force it into an approved category.

## 3. License review statuses

Use these statuses consistently:

| Status | Meaning |
|---|---|
| `LICENSE_PENDING_REVIEW` | Rights or evidence have not yet been reviewed |
| `LICENSE_REVIEW_REQUIRED` | Further evidence or clarification is needed |
| `LICENSE_APPROVED` | Evidence has been reviewed and the documented intended use is accepted |
| `LICENSE_RESTRICTED` | Use is accepted only within recorded restrictions |
| `LICENSE_REJECTED` | The intended use is not approved |

`LICENSE_APPROVED` applies only to the reviewed use and evidence. It is not a universal legal clearance.

## 4. Permitted use and restrictions

An asset may be used only within permissions supported by its applicable rights and license. Depending on those permissions, uses may include game environments, adaptation, integration into builds, and distribution as part of the complete game.

Standalone redistribution of source assets is not automatically permitted. Do not remove required notices, misrepresent third-party assets as original, or use assets beyond the scope of their permissions.

## 5. Third-party license priority

The original third-party license governs third-party material. If its terms conflict with a proposed project use, suspend that use until the conflict is resolved or appropriate permission is obtained.

## 6. AI-assisted asset policy

Retain available records of the AI tool, relevant platform terms, prompts, reference inputs, generated output, and human modifications. Record unknown information honestly. AI generation alone does not establish exclusive copyright ownership or commercial clearance.

## 7. Registry requirements

Every asset should be recorded in the VAL Asset Registry with, at minimum:

- Asset ID, name, filename, category, and version.
- Creator/provider and source.
- Provenance category and review status.
- License category and review status.
- SHA-256 checksum where applicable.
- Visual, technical, and runtime QA statuses.
- Restrictions, evidence locations, and review date.

Unknown values must be marked `UNKNOWN` or `NOT_PROVIDED`, not inferred.

## 8. Separate approval dimensions

Visual QA, technical QA, runtime QA, provenance review, license review, owner approval, and repository integration are separate decisions. Passing one does not imply passing another.

A visually approved asset is not automatically license-approved, runtime-tested, commercially cleared, or authorized for repository integration.

## 9. Commercial distribution gate

Before commercial distribution, review the rights and terms for every included asset, including third-party compatibility, AI platform terms, attribution, redistribution restrictions, and unresolved provenance questions. Assets with unresolved material rights issues must be excluded from the affected release until resolved.

## 10. Records and changes

Every license-status change must identify the asset version, supporting evidence, reviewer/owner decision, date, and updated registry entry. Preserve prior records where relevant to the audit trail. Do not modify original binaries merely to update documentation.

## 11. Disclaimer

This is an internal project policy, not legal advice. It does not guarantee copyright protection or establish rights in third-party or AI-generated material. Laws and platform terms vary and may change. Obtain qualified legal review before commercial publication or licensing where appropriate.

## 12. Version history

| Version | Change | Status |
|---|---|---|
| 1.0 | Initial VAL framework | Approved — effective 2026-11-21 |

**Document status:** APPROVED — EFFECTIVE 2026-11-21  
**Repository integration:** NOT AUTHORIZED
