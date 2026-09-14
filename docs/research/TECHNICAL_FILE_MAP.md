# Public Technical File Map

This document records **publicly reported** Sword/Shield internal paths, schemas, containers, and save structures that are useful for reconstruction planning when no local retail game dump is available.

Nothing in this file is promoted to target-level `Observed` merely because it appears in a public reverse-engineering project. Unless otherwise stated, entries are **Unverified / external evidence** under this repository's verification rules.

## Source snapshots used in this batch

- `kwsch/pkNX` snapshot: commit `d191cd0e5c05f2af81d9a41c1f1d82e6621b351a` (2026-07-16 UTC).
- `kwsch/PKHeX` code-search snapshot: commit `fd213a27db65d6223bcf47935e36c7d375e04b7b`.
- Switch-Toolbox Pokémon Sword/Shield model workflow wiki.
- `SciresM/hactool` platform-level Nintendo Switch container reference.

Pinned upstream snapshots are used so that later research can reproduce what this repository actually inspected.

## Sword/Shield file-map leads from pkNX

### Localized messages

`GameFileMapping.cs` reports `common` and `script` message trees beneath `bin/message/` for these internal language labels:

| Internal label | Reported role |
| --- | --- |
| `JPN` | Japanese common/script messages |
| `JPN_KANJI` | Japanese kanji common/script messages |
| `English` | English common/script messages |
| `French` | French common/script messages |
| `Italian` | Italian common/script messages |
| `German` | German common/script messages |
| `Spanish` | Spanish common/script messages |
| `Korean` | Korean common/script messages |
| `Simp_Chinese` | Simplified Chinese common/script messages |
| `Trad_Chinese` | Traditional Chinese common/script messages |

The mapping source also comments an unused language index between German and Spanish. This is a technical lead, not yet a target-verified statement.

### Core Pokémon data

| Logical data | Publicly reported path / container |
| --- | --- |
| Item data | `bin/pml/item/item.dat` |
| Evolution data | `bin/pml/evolution/` |
| Egg moves | `bin/pml/tamagowaza/` |
| Personal/species data | `bin/pml/personal/` |
| Move data | `bin/pml/waza/` |
| Level-up learnsets | `bin/pml/waza_oboe/wazaoboe_total.bin` |
| Item hash/index mapping | `bin/pml/item/item_hash_to_index.dat` |

These paths provide the first public roadmap for reconstructing editable `data/` representations later. File counts, per-version byte layouts, hashes, and Sword-vs-Shield differences remain `TBD`.

### Scripted encounters and rentals

| Logical data | Publicly reported path |
| --- | --- |
| Static/event encounters | `bin/script_event_data/event_encount_data.bin` |
| In-game trades | `bin/script_event_data/field_trade.bin` |
| Gift/add Pokémon | `bin/script_event_data/add_poke.bin` |
| Rentals | `bin/script_event_data/rental.bin` |

### Battle Tower

| Logical data | Publicly reported path |
| --- | --- |
| Battle Tower Pokémon | `bin/field/param/battle_tower/battle_tower_poke_table.bin` |
| Battle Tower trainers | `bin/field/param/battle_tower/battle_tower_trainer_table.bin` |

The inspected pkNX snapshot also contains FlatBuffers schema files named `BattleTowerPoke.fbs` and `BattleTowerTrainer.fbs` under `FlatBuffers/SWSH/Schemas/`.

### Wild encounters, nests, placement, and Dynamax-related data

| Logical data | Publicly reported path / container |
| --- | --- |
| Wild encounter data | `bin/archive/field/resident/data_table.gfpak` |
| Nest/raid data | `bin/archive/field/resident/data_table.gfpak` |
| Field placement | `bin/archive/field/resident/placement.gfpak` |
| Dynamax den table | `bin/appli/chika/data_table/underground_exploration_poke.bin` |
| Symbol encounter behavior | `bin/field/param/symbol_encount_mons_param/symbol_encount_mons_param.bin` |

The public schema tree additionally exposes files with names such as `EncounterArchive.fbs`, `EncounterNestArchive.fbs`, `EncounterStaticArchive.fbs`, and `EncounterTradeArchive.fbs`. Their existence strongly identifies research areas, but their semantic completeness and exact correspondence to every retail update remain unverified here.

### Shops and other application data

| Logical data | Publicly reported path |
| --- | --- |
| Shop data | `bin/appli/shop/bin/shop_data.bin` |

The current file-map source comments `bin/demo` for cutscenes and `bin/archive/pokemon` for models. These are leads for later container and asset surveys.

## Asset-format leads

Switch-Toolbox's public Sword/Shield model workflow reports model files using `.gfbmdl`, with many models stored inside `.gfpak` archives. The guide discusses Pokémon, maps, NPC/trainer models, and objects.

For this project, that information is sufficient to open a format-research queue, but not to claim complete format coverage. Animation, texture, material, skeleton, compression, archive-index, and version-difference research still require separate evidence.

## Nintendo Switch container context

`hactool` publicly documents support for Switch formats including NCA, PFS0/ExeFS, RomFS, NPDM, NSO0, and related containers. This is **platform-level evidence** that informs terminology and extraction architecture. It does not establish which specific Sword files or executable modules exist in a given target build.

Because this project has no dump and does not store keys, there is currently no repository-local NCA/ExeFS/RomFS extraction evidence.

## Save-format leads from PKHeX

PKHeX contains `PKHeX.Core/Saves/SAV8SWSH.cs`, described in source as the Generation 8 save object for Sword/Shield. Public code search also exposes Sword/Shield save substructures such as daycare, fused Pokémon storage, and Pokédex handling.

This establishes PKHeX as a major public lead for save-block and PK8 research. Exact block hashes/keys, revision handling, encrypted/decrypted size claims, and update-specific save differences must be inventoried from pinned source files before being transferred into this repository's own structured documentation.

## Public schema categories observed in pkNX

The `FlatBuffers/SWSH/Schemas/` directory at the pinned snapshot includes public schema names covering at least these research areas:

- archive content
- Battle Tower Pokémon/trainers
- camp-related tables
- field/cell tables
- wild encounters
- nest encounters
- static encounters
- trades
- placement-related structures

This is not yet a complete schema inventory. A later batch should enumerate the directory recursively into a machine-readable manifest with each upstream path, blob SHA, inferred category, and repository verification status.

## Reconstruction implications

The current public evidence is already sufficient to justify future repository material in these existing top-level areas once concrete work begins:

- `data/` for reconstructed editable tables and schemas
- `include/` for stable identifiers/constants derived from independently verified research
- `tools/` for parsers/converters written or adapted with compatible licensing
- `manifests/` for upstream snapshots, source paths, hashes, and version coverage
- `docs/` for format notes and confidence tracking
- `assets/` only when actual reviewable/reconstructed material is legally and technically appropriate

No opaque copied game data should be introduced merely to imitate a dump.

## Immediate technical gaps

- Full recursive `pkNX` Sword/Shield schema and parser inventory.
- Exact upstream license boundaries for any code proposed for reuse rather than reimplementation.
- Complete PKHeX Sword/Shield save-block inventory pinned to a specific commit.
- Sword executable/module research from public symbol/function projects, if available.
- `.gfpak`, `.gfbmdl`, texture, animation, audio, message, and serialization format documentation from multiple independent public sources.
- Update-specific path/schema differences across Ver.1.1.0 through Ver.1.3.2.
- Sword-vs-Shield path/data differences.
- Regional/language file identity and deduplication evidence.

_Last surveyed: 2026-09-14._
