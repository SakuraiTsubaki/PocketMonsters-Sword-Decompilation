# Project Status

**Current stage:** Phase 0 — Target definition / public-source inventory

This document tracks decompilation progress, target-version coverage, validation level, and the next major milestones.

The project currently has **no locally owned retail game dump**. Work is proceeding by exhaustive public-source research, using the Japanese release as the comparison baseline and preserving regional, language, revision, update, distribution, storefront, and technical-source differences.

## Version inventory

| Target | Region | Language | Revision / update | Verification | Notes |
| --- | --- | --- | --- | --- | --- |
| Pocket Monsters Sword launch release | JP baseline | 9 languages officially supported at product level | Launch; internal version TBD | Reference only | Official Japanese release date: 2019-11-15. Hashes unavailable. |
| Pocket Monsters Sword updates | JP baseline | Binary language identity TBD | 1.1.0 → 1.3.2 | Reference only | Official Japanese update chronology seeded in `VERSIONS.md`; NA publication dates also recorded for comparison. |

## Progress

- [ ] Establish authoritative version/revision inventory
  - Japanese official launch metadata recorded.
  - Japanese official update sequence Ver.1.1.0 through Ver.1.3.2 recorded.
  - North American official update dates recorded as regional comparison metadata.
  - Official regional/storefront evidence captured for Japan, Korea, United States, Canada (English/French), United Kingdom, Spain, Netherlands, Belgium, Portugal, Australia, Brazil, and Hong Kong sale presence.
  - Taiwan, New Zealand, remaining Americas, complete EMEA coverage, physical revisions, and authoritative content identities remain in progress.
  - Cryptographic hashes and exact target identities remain unavailable without independently reproducible evidence.
- [ ] Document executable and section layout
  - Public Switch container tooling (`hactool`) is indexed for NCA/ExeFS/RomFS/NSO terminology.
  - No Sword-specific executable layout is treated as target-observed yet.
- [ ] Map symbols, functions, and major subsystems
- [ ] Document game-data formats and resource containers
  - Pinned `pkNX` source snapshot recorded.
  - Initial public Sword/Shield path map covers localized messages, PML item/evolution/egg/personal/move/learnset data, scripted encounters, trades, gifts, Battle Tower, wild/nest data, Dynamax den tables, placement, shops, rentals, symbol encounters, and item hash mapping.
  - Public SWSH FlatBuffers schema directory is identified for recursive inventory in a later batch.
- [ ] Reconstruct scripts, events, and behavior
  - Scripted encounter/trade/gift/rental file leads are documented, but no reconstruction has begun.
- [ ] Reconstruct asset pipelines and metadata
  - Switch-Toolbox Sword/Shield model documentation is indexed as external evidence for `.gfbmdl` / `.gfpak` workflows.
- [ ] Add reproducible extraction/repacking tooling
- [ ] Add automated verification where practical

## Research material added

- `docs/research/PUBLIC_SOURCE_INDEX.md` — living human-readable public-source index and evidence notes.
- `docs/research/REGION_LANGUAGE_MATRIX.md` — official regional/storefront/language evidence without assuming distinct regional binaries.
- `docs/research/TECHNICAL_FILE_MAP.md` — pinned public technical leads from pkNX, PKHeX, Switch-Toolbox, and Switch container tooling.
- `manifests/public-sources.json` — machine-readable initial source inventory.
- `manifests/regional-coverage.json` — machine-readable regional coverage state.
- `manifests/technical-source-snapshots.json` — pinned upstream technical source snapshots.
- `docs/VERSIONS.md` — seeded official version chronology with explicit unresolved regional/binary identity.

## Validation levels

- **Unverified** — proposed or recorded but not independently checked against the intended target.
- **Observed** — confirmed directly in a target build or extracted data.
- **Reproduced** — behavior or data can be recreated with documented steps.
- **Matched** — reconstructed output is verified against the intended target.
- **Reference only** — public comparison evidence exists, but target identity/hashes are not independently verified for reconstruction.

Public web pages and upstream source repositories can themselves be directly observed as sources while the game-target claims derived from them remain `Reference only` or `Unverified / external evidence` until repository verification requirements are met.

## Next milestones

1. Complete official regional inventory: Korea update-detail pages, Hong Kong Sword-specific product metadata, Taiwan, New Zealand, remaining Americas, and remaining EMEA storefront variants.
2. Catalogue physical package identifiers and game-card revisions from provenance-bearing public sources.
3. Investigate public eShop/CDN metadata for Title ID/content-identity evidence without obtaining redistributed retail binaries.
4. Recursively inventory the pinned `pkNX` Sword/Shield schemas/parsers into machine-readable manifests.
5. Inventory PKHeX Sword/Shield save blocks and PK8-related structures from a pinned source snapshot.
6. Expand format research for `.gfpak`, `.gfbmdl`, textures, animations, audio, messages, and serialization using multiple independent public sources.
7. Keep `VERSIONS.md`, the public-source manifests, and verification status synchronized as evidence improves.

Update this file whenever the project reaches a meaningful milestone or adds a new supported target.
