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
| [Japanese Official Page Enumeration](research/JP_OFFICIAL_PAGE_ENUMERATION.md) | Page-by-page Japanese official Sword/Shield news ledger; the live index declares 117 entries while 115 dated titles are currently directly observed, leaving a two-entry discrepancy under investigation |
| [Japanese Official Off-Index Sources](research/JP_OFFICIAL_OFF_INDEX_SOURCES.md) | Japanese official Sword/Shield-relevant pages discovered outside the dedicated news-index workflow |
| [Japanese Distribution Source Ledger](research/JP_DISTRIBUTION_SOURCE_LEDGER.md) | Pokémon, item, clothing, Dynamax Crystal, HOME-linked and other Japanese official distribution evidence |
| [Japanese Pokémon HOME Integration Ledger](research/JP_HOME_INTEGRATION_LEDGER.md) | HOME version chronology, Sword/Shield transfer behavior and cross-title interoperability evidence |
| [Japanese Competition and Online-Service Ledger](research/JP_COMPETITION_ONLINE_LEDGER.md) | Battle Stadium, Internet Competitions, championship paths, competition bugs and final online-service state |
| [Official Regional Site Map](research/OFFICIAL_REGIONAL_SITE_MAP.md) | Region-by-region official Sword/Shield publication surfaces for Japanese-baseline comparison |
| [Region and Language Matrix](research/REGION_LANGUAGE_MATRIX.md) | Official regional/storefront/language evidence separated from unresolved binary identity |
| [Public Reverse-Engineering Repository Catalog](research/PUBLIC_REPOSITORY_CATALOG.md) | Primary public technical repositories, archive state, research scope, and fork-handling rules |
| [Public Technical File Map](research/TECHNICAL_FILE_MAP.md) | Pinned external reverse-engineering leads for Sword/Shield paths, schemas, save data, and Switch containers |
| [Project Pokémon Generation VIII Event Archive Survey](research/PROJECT_POKEMON_GEN8_EVENT_ARCHIVE.md) | Secondary event/Wonder Card/BCAT archive coverage; 215 Sword/Shield records require individual enumeration and primary-source cross-checking |
| [Research Guide](RESEARCH_GUIDE.md) | Evidence, confidence, offsets, naming, and research-recording practices |
| [Verification Guide](VERIFICATION.md) | Standards for Unverified, Observed, Reproduced, and Matched results |
| [Repository Structure](REPOSITORY_STRUCTURE.md) | Intended long-term layout for source, data, assets, tools, tests, and manifests |
| [Project Standards](PROJECT_STANDARDS.md) | Naming, provenance, generated-data, manifest, and repository-boundary rules |
| [Asset Workflow](ASSET_WORKFLOW.md) | Extraction, reviewable assets, deduplication, manifest registration, and batch workflow |
| [Manifest Guide](../manifests/README.md) | Machine-readable inventories, hashes, target coverage, provenance, and shared assets |
| [Contributing](../CONTRIBUTING.md) | Contribution rules, evidence expectations, commits, and pull-request guidance |

## Research areas

As verified work becomes concrete, documentation may grow into areas such as `architecture/`, `formats/`, `research/`, `versions/`, and `verification/`. Create these directories when they contain real research material rather than as empty placeholders.

`research/` now contains active public-source, Japanese-official-page, off-index official-source, distribution, HOME, competition/online, regional/language, regional-site, public-repository, technical file-map, event-archive, and exhaustive source-coverage surveys because concrete research material is available. Additional subdirectories should still be created only when they contain real project material.

## Recommended documentation flow

1. Identify the target in `VERSIONS.md`.
2. Consult `research/SOURCE_COVERAGE_TRACKER.md` first to determine which source families are still incomplete.
3. Consult `research/PUBLIC_SOURCE_INDEX.md` for current public-source provenance and unresolved coverage gaps.
4. Use `research/JP_OFFICIAL_PAGE_ENUMERATION.md` and `../manifests/jp-official-news-index.json` when working through the Japanese dedicated news corpus. Preserve the current **117 declared / 115 directly observed / 2 unresolved** count discrepancy until the missing records are actually located.
5. Use `research/JP_OFFICIAL_OFF_INDEX_SOURCES.md` and `../manifests/jp-off-index-official-sources.json` for Japanese official material outside the dedicated Sword/Shield index.
6. Use `research/JP_DISTRIBUTION_SOURCE_LEDGER.md` with `../manifests/jp-distribution-sources.json`, and `research/PROJECT_POKEMON_GEN8_EVENT_ARCHIVE.md`, when researching distributions. Official campaign provenance and external Wonder Card/BCAT evidence must remain distinguishable.
7. Use `research/JP_HOME_INTEGRATION_LEDGER.md` with `../manifests/jp-home-sources.json` for HOME versioning, transfer restrictions and cross-title behavior.
8. Use `research/JP_COMPETITION_ONLINE_LEDGER.md` with `../manifests/jp-competition-online-sources.json` for Battle Stadium, competitions, ranked rules, service lifecycle and competition-linked bugs/rewards.
9. Use `research/OFFICIAL_REGIONAL_SITE_MAP.md` and `research/REGION_LANGUAGE_MATRIX.md` when comparing official regional releases, websites, storefronts, languages, ratings, promotions, and package-facing metadata.
10. Use `research/PUBLIC_REPOSITORY_CATALOG.md`, `../manifests/public-repositories.json`, and `research/TECHNICAL_FILE_MAP.md` for public reverse-engineering leads, while preserving their external-evidence status until independently verified.
11. Record investigation methods and evidence according to `RESEARCH_GUIDE.md`.
12. Reconstruct source, data, or assets following `PROJECT_STANDARDS.md` and `REPOSITORY_STRUCTURE.md`.
13. For asset work, follow `ASSET_WORKFLOW.md` and register material in `../manifests/`.
14. Apply the validation levels defined in `VERIFICATION.md`.
15. Update `PROJECT_STATUS.md` and `ROADMAP.md` when meaningful milestones are reached.

## Documentation rules

- A representative sample is never sufficient for a source family marked for exhaustive survey.
- Do not call a source family complete merely because its best-known sources were indexed; use the states in `research/SOURCE_COVERAGE_TRACKER.md`.
- A declared count and an actually enumerated count are separate facts. Count discrepancies must remain explicit until resolved.
- Discovery surfaces are not assumed complete: dedicated game sites, general Pokémon/Nintendo news, regional sites, support pages, videos, PDFs, retailer campaigns, archives, and public research repositories must be searched separately.
- Forks and mirrors are not independent confirmations unless they contain materially distinct research or preserved history.
- Official campaign prose, Wonder Card/internal event data, and community archival metadata are separate evidence layers and must not be silently merged.
- Current HOME documentation must not be projected backwards onto older HOME versions without contemporaneous evidence.
- Distinguish confirmed findings from hypotheses.
- Identify the exact target version or revision for version-specific claims.
- Record offsets, paths, symbols, hashes, commands, and other stable evidence when practical.
- Use `TBD`, `unknown`, or `null` instead of inventing missing information.
- Preserve enough provenance for another researcher to reproduce or verify the finding.
- Keep retail ROM images, decrypted game images, console keys, and other redistributable game binaries out of the repository.
