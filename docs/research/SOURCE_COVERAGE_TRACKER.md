# Exhaustive Public-Source Coverage Tracker

This document prevents a seed list of sources from being mistaken for a completed survey.

The project has **no locally owned retail dump**, so public-source reconstruction is itself a primary workstream. The survey baseline is the **Japanese release**, but completion requires systematic comparison against every discoverable official regional/language source and every materially relevant public technical/research source.

## Completion vocabulary

- **Not started** — source family identified but not yet enumerated.
- **Enumerating** — discovery/indexing is underway; the family is not complete.
- **Indexed** — known items have individual records/links, but contents have not all been reviewed.
- **Reviewed** — every indexed item has been read/classified and relevant claims/data extracted.
- **Cross-checked** — reviewed findings have been compared against independent evidence where practical.
- **Exhausted** — no additional material was found after repeated searches using alternate names, languages, domains, archives, and related-project references. This is a research-state label, not a claim that the Internet can be proven globally complete forever.

No family may be described as complete before it reaches at least **Reviewed**, and technical claims remain subject to the verification levels in `../VERIFICATION.md`.

## A. Official Japanese baseline

| Source family | Known minimum / anchor | Status | Required completion work |
| --- | ---: | --- | --- |
| Sword/Shield official `news` index | **117 entries** (70 game-information + 47 campaign entries shown by the official index) | Enumerating | Create one record per entry; preserve date, title, URL, category, subject, affected game/version, distribution/raid/competition/update flags, and archived-state notes |
| Official story/world pages | multiple | Not started | Enumerate every page and revision discoverable from navigation and archived snapshots |
| Official gameplay/system pages | multiple | Not started | Enumerate Dynamax, Gigantamax, Wild Area, Max Raid, Y-Comm, Battle Stadium, Camp, jobs, League Card, etc. |
| Official Pokémon pages | multiple | Not started | Enumerate species/form reveals, version-exclusive presentation, pre-release wording changes |
| Official character pages | multiple | Not started | Enumerate characters, Gym/version differences, updated profiles |
| Product/bonus pages | multiple | Enumerating | Package/download/double-pack, preorder, retailer bonuses, Poké Ball Plus, bundled Expansion Pass releases |
| Expansion Pass official site/pages | multiple | Not started | Isle of Armor and Crown Tundra pages, announcements, keywords, trailers, purchase bonuses |
| Japanese update notices | 1.1.0–1.3.2 known | Indexed | Review every notice and compare wording/date against other regions |
| Japanese distributions | many | Enumerating | Serial-code, local, movie, store, Mystery Gift, save-link and campaign distributions |
| Japanese Wild Area / Max Raid events | many | Enumerating | Individual event chronology, encounter changes, periods, version differences, BCAT linkage where publicly documented |
| Japanese online competitions / Battle Stadium | many | Not started | Rules, seasons, bans, rewards, dates and service changes |
| Japanese HOME-related notices | multiple | Not started | HOME launch/compatibility changes, transfer restrictions, gifts |
| Japanese support/FAQ | multiple | Not started | Error notices, online requirements, save/DLC troubleshooting |
| Official videos / Pokémon YouTube | many | Enumerating | Initial reveal, NEWS #01–#10, final PV, DLC trailers, event videos; retain publication metadata and version-dependent footage observations |
| Pre-release screenshots / press assets | many | Not started | Catalogue official screenshots and identify differences from retail only when evidence supports it |

## B. Official regional and language sources

Each region is tracked separately from software-language support. A storefront region does **not** imply a distinct executable/content build.

| Region/source family | Status | Required work |
| --- | --- | --- |
| Korea — Nintendo Korea / Pokémon Korea | Enumerating | Full product, news, patch, event, distribution, competition, DLC, HOME and support sweep in Korean |
| North America — Nintendo US / Pokémon US | Enumerating | Product/SKU, support, update, event, competition, DLC, HOME, press/news |
| Canada English | Enumerating | Store/support/product differences and Canada-specific promotions |
| Canada French | Enumerating | French-Canadian product/support/promotional differences |
| UK | Enumerating | Nintendo UK / Pokémon UK pages, PEGI-facing metadata, events/promotions |
| France | Not started | French official product/news/support/events |
| Germany | Not started | German official product/news/support/events |
| Italy | Not started | Italian official product/news/support/events |
| Spain | Not started | Spanish official product/news/support/events |
| Netherlands | Not started | Dutch storefront/product/support presentation |
| Belgium | Not started | Regional storefront/product metadata |
| Portugal | Not started | Regional storefront/product metadata |
| Australia | Enumerating | ACB-facing product/support/events |
| New Zealand | Not started | Product/support/regional promotions |
| Hong Kong | Enumerating | Traditional-Chinese official pages, product/distribution/support |
| Taiwan | Not started | Traditional-Chinese official pages, product/distribution/support |
| Mainland/Chinese-language official material | Not started | Simplified-Chinese official presentation where officially published |
| Latin America / Mexico / Brazil | Enumerating | Nintendo/Pokémon regional product/promotional/support pages; distinguish Spanish/Portuguese localization from storefront region |
| Other official Nintendo/Pokémon regions discoverable via region selectors/archives | Not started | Enumerate rather than assume absence |

## C. Public reverse-engineering / decompilation-adjacent sources

| Project/source | Coverage | Status |
| --- | --- | --- |
| `kwsch/pkNX` | RomFS/ExeFS file mappings, FlatBuffers schemas, editors, encounter/raid/trainer/text/PML/placement/shop data | Enumerating |
| `kwsch/PKHeX` | `SAV8SWSH`, PK8, save blocks, legality, encounters, events, HOME remapping | Enumerating |
| `KillzXGaming/Switch-Toolbox` | `.gfpak`, `.gfbmdl`, textures/models/material workflows and related Game Freak formats | Enumerating |
| `ChicoEevee/Pokemon-Switch-Model-Importer-Blender` | model/animation research and Blender import/export | Indexed |
| `Shararamosh/io_scene_gfbanm` | `.gfbanm` animation format import/export research | Indexed |
| `SciresM/hactool` | Switch NCA/ExeFS/RomFS/NSO platform container context | Indexed |
| Switchbrew / libnx / Atmosphère technical documentation | Switch runtime/platform context needed to understand public memory/hook research | Not started |
| `lincoln-lm/swsh-mods-exl` | Sword/Shield 1.3.2 ExeFS hooks, encounter runtime behavior, message paths, configs | Indexed |
| other forks/precursors/referenced mods of `swsh-mods-exl` | historical hook discoveries and attribution trail | Not started |
| `KotMatrosk1n/KM-Editor` | modern Sword/Shield editor coverage; verified data ownership/path documentation in wiki/releases | Indexed |
| `zaksabeast/CaptureSight` | RAM structures, raid/wild/trade views, RNG state observations | Indexed |
| `Admiral-Fish/RaidFinder` | Max Raid RNG algorithm/tooling | Indexed |
| `Leanny/PKHeX_Raid_Plugin` | raid save data and RNG tooling | Indexed |
| `zaksabeast/PokemonRNGGuides` | Sword/Shield RNG guides and derivations | Not started |
| `lincoln-lm/swsh-rng-tool` | Sword/Shield RNG research/tooling | Indexed |
| `kwsch/SysBot.NET` | Sword/Shield seed-check/trade automation research | Indexed |
| Lusamine public research gists/catalog | SWSH overworld RNG and other reverse-engineering notes | Indexed |
| additional GitHub repositories discovered through code/repository search | unknown | Enumerating |

### Fork handling

Forks are **not** automatically counted as independent evidence. A fork becomes a separate source record only when it contains materially different research, commits, documentation, preserved history, or otherwise unavailable data.

## D. Events, distributions, network-delivered data

| Source family | Status | Required work |
| --- | --- | --- |
| Project Pokémon Generation VIII Event Gallery | Enumerating | Individual Sword/Shield Wonder Card/Mystery Gift entries, provenance, region/language constraints, file types |
| Project Pokémon contribution/research threads | Not started | BCAT, Wonder Card, save structure and distribution research |
| Wild Area News / BCAT research archives | Not started | Event-table versions, periods, raid pools, hashes/identifiers when publicly documented |
| Serebii event database | Not started | Secondary chronology and cross-check; never sole evidence for internal technical claims |
| Bulbapedia event/distribution articles | Not started | Secondary cross-check and regional naming/date differences |
| Official serial-code/store/movie campaigns by region | Enumerating | Primary evidence first; archive secondary captures if originals disappeared |

## E. Game-data databases and gameplay references

| Source family | Status | Required work |
| --- | --- | --- |
| Bulbapedia Sword/Shield and subarticles | Enumerating | Version history, mechanics, locations, trainers, glitches, unused/pre-release references; trace citations upstream |
| Serebii Sword/Shield sections | Not started | encounters, raids, trainers, items, events, version differences, DLC; cross-check against technical sources |
| Pokémon Database and other structured databases | Not started | use as discovery/cross-check only; record discrepancies |
| Smogon / Pokémon Showdown source and data | Not started | battle mechanics/test data, move/ability behavior, competitive rule changes; distinguish simulator behavior from game evidence |
| community spreadsheets/datamines with provenance | Not started | include only with traceable authorship/source and confidence labels |

## F. Bugs, glitches, unused and pre-release material

| Source family | Status | Required work |
| --- | --- | --- |
| Bulbapedia Generation VIII glitches | Indexed | Split by affected versions; find original demonstrations/research where possible |
| The Cutting Room Floor / equivalent unused-data research | Enumerating | Search Sword, Shield, DLC, prototype/trailer differences; require evidence classification |
| public datamine threads/posts | Not started | Archive/source-map only when provenance is attributable and claims can be cross-checked |
| official trailers/screenshots vs retail comparisons | Not started | Separate development-footage differences from data that actually remains unused in retail |
| patch-fixed exploits/bugs | Enumerating | link official patch note + technical/community reproduction evidence |

## G. Media, assets, formats and audio

| Source family | Status | Required work |
| --- | --- | --- |
| model formats (`gfbmdl`) | Enumerating | parsers, docs, importer/exporter implementations, model/material semantics |
| archives (`gfpak`) | Enumerating | format implementations and path conventions |
| animations (`gfbanm`) | Enumerating | import/export implementations, schema/field research |
| textures (`bntx` and Game Freak use) | Not started | format tools and game-specific conventions |
| shaders/materials | Not started | public research/tools, limitations, game-specific observations |
| maps/placement | Enumerating | pkNX schemas, editor/mod research, object placement/zone data |
| particle/effect formats | Not started | public tools/research and runtime hook references |
| audio/music/voice formats | Not started | public extraction/format research, soundtrack/official metadata, version/language differences |
| fonts/UI/localization assets | Not started | file-format/path research and region/language differences |

## H. Save, Pokémon entity, HOME and interoperability

| Source family | Status | Required work |
| --- | --- | --- |
| Sword/Shield save container/block structure | Enumerating | PKHeX + independent research, block IDs/semantics/revisions |
| PK8 structure | Enumerating | encrypted/stored/party representations, fields, legality implications |
| Pokémon HOME transfer/remap behavior | Not started | official compatibility notices + PKHeX/HOME research; version-specific behavior |
| save-data bonuses/link rewards | Not started | official primary sources by region and game linkage |
| cloud/online service changes | Not started | HOME/Nintendo/Pokémon notices and shutdown/maintenance history |

## I. Packaging, retail revisions and identifiers

| Source family | Status | Required work |
| --- | --- | --- |
| Japanese JAN/package variants | Not started | standard, double pack, Expansion Pass bundle, later prints |
| North American UPC/SKU/package variants | Enumerating | retail identifiers, ratings, label revisions |
| European EAN/package variants | Not started | PEGI/local packaging variants |
| Korean package identifiers | Enumerating | package/double-pack/bundle metadata |
| Hong Kong/Taiwan package identifiers | Not started | package languages/ratings/identifiers |
| game-card revisions / bundled-update cartridges | Not started | document only from reproducible public cartridge/revision evidence; do not distribute dumps |
| Title ID / content IDs / update IDs | Enumerating | use public technical sources; distinguish identifier evidence from possession of copyrighted content |

## J. Archived/deleted material

| Source family | Status | Required work |
| --- | --- | --- |
| Internet Archive captures of official pages | Not started | locate removed/changed official pages and record capture timestamps |
| deleted GitHub projects/forks preserved elsewhere | Not started | provenance and license review required |
| archived social posts from official accounts | Not started | only when relevant to releases/events/technical behavior and source can be authenticated |
| old wiki revisions | Not started | use when current pages erased historically important version-specific claims; cross-check upstream |

## Current minimum source findings that must not be lost

The initial sweep has already identified, among others:

- official Japanese Sword/Shield news index with **117 entries**;
- official regional Nintendo/Pokémon storefront/support sources;
- `pkNX`, including Sword/Shield file mappings and FlatBuffers schemas;
- `PKHeX`, including `SAV8SWSH` and Generation VIII save/Pokémon structures;
- Switch-Toolbox Game Freak format research;
- CaptureSight;
- RaidFinder;
- PKHeX Raid Plugin;
- SysBot.NET seed-check research;
- `swsh-mods-exl` runtime hooks for 1.3.2;
- KM Editor and its current Sword/Shield editing/technical documentation;
- Pokémon Switch model/animation Blender importers;
- Project Pokémon Event Gallery;
- Bulbapedia version-history and Generation VIII glitch catalogs;
- secondary event/gameplay databases still requiring individual enumeration.

## Rule for future work

A research session should **add newly discovered sources to the index even when no substantive data has yet been extracted from them**. Discovery and interpretation are separate stages. This ensures later searches can determine whether a source family was genuinely exhausted or merely overlooked.

_Last updated: 2026-09-14._
