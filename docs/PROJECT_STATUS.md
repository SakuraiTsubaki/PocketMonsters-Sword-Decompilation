# Project Status

**Current stage:** Phase 0 — Target definition / exhaustive public-source census

This document tracks decompilation progress, target-version coverage, validation level, and the next major milestones.

The project currently has **no locally owned retail game dump**. Work is proceeding by exhaustive public-source research, using the Japanese release as the comparison baseline and preserving regional, language, revision, update, distribution, storefront, online-service, HOME, archival, and technical-source differences.

## Version inventory

| Target | Region | Language | Revision / update | Verification | Notes |
| --- | --- | --- | --- | --- | --- |
| Pocket Monsters Sword launch release | JP baseline | 9 languages officially supported at product level | Launch; internal version TBD | Reference only | Official Japanese release date: 2019-11-15. Hashes unavailable. |
| Pocket Monsters Sword updates | JP baseline | Binary language identity TBD | 1.1.0 → 1.3.2 | Reference only | Official Japanese update chronology recorded in `VERSIONS.md`; regional publication dates are retained separately. |
| Pokémon HOME linked environment | JP baseline + later cross-title state | HOME localization set tracked separately | HOME launch → relevant 1.x updates → 2.0.0 | Reference only | Sword/Shield, Isle of Armor, Crown Tundra, BDSP and PLA interoperability sources are being versioned instead of treated as one timeless rule set. |

## Exhaustive-source census progress

- **Japanese dedicated Sword/Shield news index:** official page declares 117 entries; **115 dated titles are directly observed in the current live rendering** and individually enumerated in `manifests/jp-official-news-index.json`; the unresolved two-entry discrepancy remains explicit.
- **Japanese official off-index corpus:** general Pokémon official news, Pokémon Center, retailer, movie/anime, distribution and campaign pages are being separately enumerated because the dedicated 117-entry index is not the complete official corpus.
- **Regional official sites:** confirmed official publication surfaces are being mapped separately for United States, Canada EN/FR, UK/Ireland, France, Germany, Italy, Spain, Belgium FR/NL, Netherlands, Portugal, Russia, Australia/New Zealand, Latin America and other region-selector targets. A regional website is not assumed to imply a distinct retail binary.
- **Japanese distributions:** Pokémon, item, clothing, Dynamax Crystal, movie, retailer, birthday and HOME-linked distributions are being split into individual records rather than treating “event Pokémon” as the whole distribution category.
- **Pokémon HOME:** launch and Sword/Shield-relevant Japanese official version history is seeded through HOME Ver.2.0.0; current transfer/move rules are documented with an explicit warning not to project current behavior backwards without contemporary evidence.
- **Competition / online services:** Battle Stadium, Internet/Live/Friendly competitions, tournament paths, competition-specific bugs and the 2022 final continuing online-service state are now separate research targets.
- **Project Pokémon Generation VIII archive:** the current archive reports 243 Generation VIII records, including **215 Sword/Shield records**. All 215 require individual classification and primary-source cross-checking before this source family can be considered reviewed.
- **Public reverse-engineering repositories:** primary/high-value repositories and major fork families are now catalogued so forks are not double-counted as independent evidence.

## Technical research progress

- [ ] Establish authoritative version/revision inventory
  - Japanese official launch metadata recorded.
  - Japanese official update sequence Ver.1.1.0 through Ver.1.3.2 recorded.
  - Regional publication/storefront evidence is being expanded without assuming byte-identical or distinct binaries prematurely.
  - Physical revisions, exact Title/content identities and cryptographic hashes remain unresolved pending provenance-bearing public evidence.
- [ ] Document executable and section layout
  - Public Switch container tooling (`hactool`) is indexed for NCA/ExeFS/RomFS/NSO terminology.
  - `swsh-mods-exl` and related ExeFS patches are indexed as runtime/executable research leads.
  - No Sword-specific executable layout is treated as target-observed yet.
- [ ] Map symbols, functions, and major subsystems
  - Runtime/RNG research sources including CaptureSight, RaidFinder, SysBot.NET, PokémonRNGGuides and `swsh-rng-tool` are catalogued for later recursive review.
- [ ] Document game-data formats and resource containers
  - Pinned `pkNX` source snapshot recorded.
  - Initial public Sword/Shield path map covers localized messages, PML item/evolution/egg/personal/move/learnset data, scripted encounters, trades, gifts, Battle Tower, wild/nest data, Dynamax den tables, placement, shops, rentals, symbol encounters, and item hash mapping.
  - Public SWSH FlatBuffers schema directory is identified for recursive inventory.
  - Switch-Toolbox, Pokémon Switch Model Importer and `io_scene_gfbanm` are catalogued for model/texture/material/animation research.
- [ ] Reconstruct scripts, events, and behavior
  - Scripted encounter/trade/gift/rental file leads are documented, but no target-verified reconstruction has begun.
- [ ] Reconstruct asset pipelines and metadata
  - Asset tooling and format leads are indexed; direct retail-derived assets are not assumed available or redistributable.
- [ ] Add reproducible extraction/repacking tooling
- [ ] Add automated verification where practical

## Active research documents

- `docs/research/PUBLIC_SOURCE_INDEX.md`
- `docs/research/SOURCE_COVERAGE_TRACKER.md`
- `docs/research/JP_OFFICIAL_PAGE_ENUMERATION.md`
- `docs/research/JP_OFFICIAL_OFF_INDEX_SOURCES.md`
- `docs/research/JP_DISTRIBUTION_SOURCE_LEDGER.md`
- `docs/research/JP_HOME_INTEGRATION_LEDGER.md`
- `docs/research/JP_COMPETITION_ONLINE_LEDGER.md`
- `docs/research/OFFICIAL_REGIONAL_SITE_MAP.md`
- `docs/research/REGION_LANGUAGE_MATRIX.md`
- `docs/research/PUBLIC_REPOSITORY_CATALOG.md`
- `docs/research/PROJECT_POKEMON_GEN8_EVENT_ARCHIVE.md`
- `docs/research/TECHNICAL_FILE_MAP.md`

## Active machine-readable inventories

- `manifests/public-sources.json`
- `manifests/source-coverage.json`
- `manifests/jp-official-news-index.json`
- `manifests/jp-off-index-official-sources.json`
- `manifests/jp-distribution-sources.json`
- `manifests/jp-home-sources.json`
- `manifests/jp-competition-online-sources.json`
- `manifests/regional-coverage.json`
- `manifests/public-repositories.json`
- `manifests/technical-source-snapshots.json`

## Validation levels

- **Unverified** — proposed or recorded but not independently checked against the intended target.
- **Observed** — confirmed directly in a specific target build or extracted target data.
- **Reproduced** — behavior or data can be recreated with documented steps.
- **Matched** — reconstructed output is verified against the intended target using an explicit exact-match criterion.
- **Reference only** — public comparison evidence exists, but target identity/hashes are not independently verified for reconstruction.

Public web pages and upstream source repositories can themselves be directly observed as sources while retail-game claims derived from them remain `Reference only` or `Unverified / external evidence` until repository verification requirements are met.

## Immediate next milestones

1. Resolve the **117 declared / 115 observed** Japanese official news-index discrepancy without inventing the missing records.
2. Continue enumerating Japanese official material outside the dedicated game site: distributions, competitions, HOME, Pokémon Center, movie/anime tie-ins, PDFs, retailer campaigns, videos and removed/archived pages.
3. Enumerate all **215** Project Pokémon Sword/Shield Generation VIII archive records into a machine-readable classification/cross-check ledger.
4. Complete every official regional Sword/Shield site route and then compare each page against the Japanese baseline, including localization-specific terminology such as the official `Terms` pages.
5. Recursively inventory the pinned `pkNX` Sword/Shield schemas/parsers into machine-readable manifests.
6. Inventory PKHeX Sword/Shield save blocks, PK8 structures, legality/encounter logic and HOME remapping from pinned source revisions.
7. Build complete Max Raid / Wild Area News / BCAT chronology from official notices plus public event-data archives.
8. Enumerate every official Internet Competition, Ranked Battle season/rules series and participation reward through the final Sword/Shield online-service state.
9. Catalogue physical package identifiers and game-card revisions from provenance-bearing public sources.
10. Investigate public eShop/CDN metadata for Title ID/content-identity evidence without obtaining redistributed retail binaries.
11. Expand format research for `.gfpak`, `.gfbmdl`, textures, animations, audio, messages and serialization using multiple independent public sources.
12. Keep `VERSIONS.md`, all source manifests, and verification status synchronized as evidence improves.

Update this file whenever the project reaches a meaningful milestone or adds a new supported target.
