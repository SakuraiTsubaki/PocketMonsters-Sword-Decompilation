# Project Status

**Current stage:** Phase 0 — Target definition / public-source inventory

This document tracks decompilation progress, target-version coverage, validation level, and the next major milestones.

The project currently has **no locally owned retail game dump**. Work is proceeding by exhaustive public-source research, using the Japanese release as the comparison baseline and preserving regional, language, revision, update, distribution, and storefront differences.

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
  - Remaining regional storefront/package/revision inventory is in progress.
  - Cryptographic hashes and exact target identities remain unavailable without independently reproducible evidence.
- [ ] Document executable and section layout
  - Public Switch container tooling and external Sword/Shield file-map sources have been indexed; target-specific claims remain unverified.
- [ ] Map symbols, functions, and major subsystems
- [ ] Document game-data formats and resource containers
  - `pkNX` is indexed as a high-priority external source for mapped Sword/Shield paths and data structures.
- [ ] Reconstruct scripts, events, and behavior
- [ ] Reconstruct asset pipelines and metadata
  - Switch-Toolbox Sword/Shield model documentation is indexed as external evidence.
- [ ] Add reproducible extraction/repacking tooling
- [ ] Add automated verification where practical

## Research material added

- `docs/research/PUBLIC_SOURCE_INDEX.md` — living human-readable public-source index and evidence notes.
- `manifests/public-sources.json` — machine-readable source inventory.
- `docs/VERSIONS.md` — seeded official version chronology with explicit unresolved regional/binary identity.

## Validation levels

- **Unverified** — proposed or recorded but not independently checked.
- **Observed** — confirmed directly in a target build or extracted data.
- **Reproduced** — behavior or data can be recreated with documented steps.
- **Matched** — reconstructed output is verified against the intended target.
- **Reference only** — public comparison evidence exists, but target identity/hashes are not independently verified for reconstruction.

## Next milestones

1. Expand the official regional inventory beyond Japan and North America, starting with Korea, Hong Kong/Taiwan, Europe/UK, Australia/New Zealand, and other official Nintendo/Pokémon storefront/support regions.
2. Build a region/language/storefront comparison matrix without assuming separate binaries.
3. Inventory launch and later physical game-card revisions from public, provenance-bearing sources.
4. Begin a structured public technical file map from `pkNX`, PKHeX, Switch-Toolbox, and additional independently discovered sources.
5. Keep `VERSIONS.md`, the public-source manifest, and verification status synchronized as evidence improves.

Update this file whenever the project reaches a meaningful milestone or adds a new supported target.
