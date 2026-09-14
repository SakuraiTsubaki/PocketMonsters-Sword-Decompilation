# Public Reverse-Engineering Repository Catalog

This catalog tracks public repositories that materially contribute to the ROM-less reconstruction of **Pokémon Sword / Shield**.

Repository existence, default branch, and archive state are observed from GitHub. Claims about the retail game that are learned from these repositories remain **external evidence** until independently reproduced or cross-checked under this project's verification rules.

## Primary and high-value repositories

| Repository | Role | Current public state | Sword/Shield relevance |
| --- | --- | --- | --- |
| `kwsch/pkNX` | Primary reverse-engineering/editor source | Active, `master` | RomFS mappings, FlatBuffers schemas, messages, PML data, encounters, raids, trainers, Battle Tower, placement, shops and other game-data structures |
| `kwsch/PKHeX` | Primary save/Pokémon-structure source | Active, `master` | `SAV8SWSH`, PK8, save blocks, Pokédex, legality, encounters, events, HOME-related handling |
| `KillzXGaming/Switch-Toolbox` | Primary asset/tool source | Active, `master` | Game Freak archive/model/texture/material workflows, including formats used by Switch Pokémon titles |
| `zaksabeast/CaptureSight` | Runtime/RNG research | Active, `main` | Runtime memory inspection, Pokémon/raid/wild information and RNG-state research |
| `Admiral-Fish/RaidFinder` | Historical raid RNG research | **Archived**, `master` | Max Raid seed search and raid-generation research; preserved as historical technical evidence |
| `Leanny/PKHeX_Raid_Plugin` | Raid save/RNG research | Active, `master` | Raid save structures, event raid data and RNG tooling around PKHeX |
| `kwsch/SysBot.NET` | Runtime automation research | Active, `master` | Memory access, trade automation and seed-check/runtime research useful for understanding SWSH behavior |
| `lincoln-lm/swsh-mods-exl` | ExeFS/runtime hook research | Active, `main` | Sword/Shield 1.3.2 hooks, encounter behavior, message/runtime configuration and executable patch research |
| `lincoln-lm/swsh-overworld-shiny-patch` | Related runtime patch | Active, `main` | Overworld encounter/shiny behavior and executable patching |
| `lincoln-lm/swsh-camera-tweaks-patch` | Related runtime patch | Active, `main` | Camera behavior and executable patching |
| `KotMatrosk1n/KM-Editor` | Modern editor/research source | Active, `master` | Sword/Shield editing coverage, data paths and format knowledge; source details require continued review |
| `ChicoEevee/Pokemon-Switch-Model-Importer-Blender` | Model/animation tool | Active, `main` | Pokémon Switch model and animation import/export research |
| `Shararamosh/io_scene_gfbanm` | Animation-format tool | Active, `master` | `.gfbanm` animation import/export research |
| `zaksabeast/PokemonRNGGuides` | RNG documentation corpus | Active, `main` | RNG methodology and Sword/Shield-specific RNG guides; individual SWSH pages still require enumeration |
| `lincoln-lm/swsh-rng-tool` | SWSH RNG tooling | Active, `main` | Sword/Shield RNG research and tooling |
| `SciresM/hactool` | Nintendo Switch platform reference | Active | NCA/NSO/RomFS/ExeFS container context; platform evidence rather than Sword-specific evidence |

## Fork policy and discovered fork families

Repository search exposes many forks and similarly named copies. They are **not** counted as independent confirmation merely because GitHub search returns them.

Fork families currently requiring historical/diff review include:

- CaptureSight: `Insektaure/CaptureSight`, `PMArkive/CaptureSight`, `auggeythecat/CaptureSight-recompiled`, and others.
- PKHeX Raid Plugin: `wubinwww/PKHeX_Raid_Plugin_chs`, `santacrab2/PKHeX_Raid_Plugin`, and others.
- SysBot.NET: `Lusamine/SysBot.NET` and other forks.
- `swsh-mods-exl`: multiple forks including `0528wcl`, `guieCo`, `OmegaPoteto` and others.
- Pokémon Switch Model Importer: multiple copies/forks including `Hengle` and `TseKaHing` variants.
- `io_scene_gfbanm`: copies/forks including `Manurocker95` and `hengtek`.
- PokémonRNGGuides: historical/translated forks including `PMArkive`, `lincoln-lm` and `HaKu76/PokemonRNGGuides_CHN`.
- Switch-Toolbox: multiple forks including `ranidspace`, `theboy181`, `Mets3D` and others.

A fork is promoted to a separate research source only when a diff/history review shows materially distinct Sword/Shield research, preserved commits unavailable upstream, a meaningful translation, documentation, or technical additions.

## Important archive-state distinction

`Admiral-Fish/RaidFinder` is currently archived. This does **not** reduce its historical research value, but it means its claims and algorithms should be associated with the versions and knowledge state for which they were developed rather than treated as a currently maintained compatibility guarantee.

## License discipline

The current catalog records a license only where it has already been explicitly verified. `kwsch/pkNX` is recorded as GPL-3.0. Other repositories remain `TBD` in the machine-readable manifest until their repository license/source headers are individually reviewed. Unknown license status means **do not copy code into this project**; link, cite, and independently document findings instead.

## Next repository-level work

For every primary repository, continue with:

1. pinning a specific reviewed commit or tag;
2. enumerating all Sword/Shield-relevant paths rather than only README-level features;
3. recording format/schema/function coverage;
4. following references and attribution to earlier projects;
5. checking forks for unique history or research;
6. recording version-specific assumptions (especially Sword/Shield 1.3.2 runtime hooks);
7. cross-checking claims against another public source where practical.

**Status: Enumerating — not complete.**

_Last updated: 2026-09-14._
