# Documentation Hub

This directory is the central documentation portal for the decompilation project. Use it to move from target identification and research through reconstruction, asset handling, manifests, and verification without losing version context or evidence.

## Quick links

| Document | Purpose |
| --- | --- |
| [Project Status](PROJECT_STATUS.md) | Current stage, target coverage, validation level, and next milestones |
| [Roadmap](ROADMAP.md) | Recommended project phases from target definition through reproducible reconstruction |
| [Version Coverage](VERSIONS.md) | Regions, languages, revisions, updates, builds, hashes, and support status |
| [Public Source Index](research/PUBLIC_SOURCE_INDEX.md) | Living ROM-less source survey using the Japanese release as baseline and preserving regional/language differences |
| [Exhaustive Source Coverage Tracker](research/SOURCE_COVERAGE_TRACKER.md) | Source-family-by-source-family completeness tracker so seed lists are never mistaken for a finished survey |
| [Japanese Official Page Enumeration](research/JP_OFFICIAL_PAGE_ENUMERATION.md) | Page-by-page ledger for the 117-entry Japanese official Sword/Shield news corpus and related official pages |
| [Region and Language Matrix](research/REGION_LANGUAGE_MATRIX.md) | Official regional/storefront/language evidence separated from unresolved binary identity |
| [Public Technical File Map](research/TECHNICAL_FILE_MAP.md) | Pinned external reverse-engineering leads for Sword/Shield paths, schemas, save data, and Switch containers |
| [Research Guide](RESEARCH_GUIDE.md) | Evidence, confidence, offsets, naming, and research-recording practices |
| [Verification Guide](VERIFICATION.md) | Standards for Unverified, Observed, Reproduced, and Matched results |
| [Repository Structure](REPOSITORY_STRUCTURE.md) | Intended long-term layout for source, data, assets, tools, tests, and manifests |
| [Project Standards](PROJECT_STANDARDS.md) | Naming, provenance, generated-data, manifest, and repository-boundary rules |
| [Asset Workflow](ASSET_WORKFLOW.md) | Extraction, reviewable assets, deduplication, manifest registration, and batch workflow |
| [Manifest Guide](../manifests/README.md) | Machine-readable inventories, hashes, target coverage, provenance, and shared assets |
| [Contributing](../CONTRIBUTING.md) | Contribution rules, evidence expectations, commits, and pull-request guidance |

## Research areas

As verified work becomes concrete, documentation may grow into areas such as `architecture/`, `formats/`, `research/`, `versions/`, and `verification/`. Create these directories when they contain real research material rather than as empty placeholders.

`research/` now contains active public-source, Japanese-official-page, regional/language, technical file-map, and exhaustive source-coverage surveys because concrete research material is available. Additional subdirectories should still be created only when they contain real project material.

## Recommended documentation flow

1. Identify the target in `VERSIONS.md`.
2. Consult `research/SOURCE_COVERAGE_TRACKER.md` first to determine which source families are still incomplete.
3. Consult `research/PUBLIC_SOURCE_INDEX.md` for current public-source provenance and unresolved coverage gaps.
4. Use `research/JP_OFFICIAL_PAGE_ENUMERATION.md` when working through the Japanese primary-source corpus; do not treat the news index alone as complete coverage.
5. Use `research/REGION_LANGUAGE_MATRIX.md` when comparing official regional releases, storefronts, languages, ratings, and package-facing metadata.
6. Use `research/TECHNICAL_FILE_MAP.md` for pinned public reverse-engineering leads, while preserving their external-evidence status until independently verified.
7. Record investigation methods and evidence according to `RESEARCH_GUIDE.md`.
8. Reconstruct source, data, or assets following `PROJECT_STANDARDS.md` and `REPOSITORY_STRUCTURE.md`.
9. For asset work, follow `ASSET_WORKFLOW.md` and register material in `../manifests/`.
10. Apply the validation levels defined in `VERIFICATION.md`.
11. Update `PROJECT_STATUS.md` and `ROADMAP.md` when meaningful milestones are reached.

## Documentation rules

- A representative sample is never sufficient for a source family marked for exhaustive survey.
- Do not call a source family complete merely because its best-known sources were indexed; use the states in `research/SOURCE_COVERAGE_TRACKER.md`.
- Distinguish confirmed findings from hypotheses.
- Identify the exact target version or revision for version-specific claims.
- Record offsets, paths, symbols, hashes, commands, and other stable evidence when practical.
- Use `TBD`, `unknown`, or `null` instead of inventing missing information.
- Preserve enough provenance for another researcher to reproduce or verify the finding.
- Keep retail ROM images, decrypted game images, console keys, and other redistributable game binaries out of the repository.
