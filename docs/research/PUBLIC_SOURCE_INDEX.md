# Public Source Index

This is the living source index for the ROM-less reconstruction of **Pocket Monsters Sword / Pokémon Sword**.

The project currently has no locally owned retail game dump. Publicly accessible evidence is therefore surveyed first, with the **Japanese release used as the comparison baseline** and all regional, language, revision, update, distribution, and storefront differences preserved rather than normalized away.

## Evidence policy

- Japanese official material is the baseline for release chronology, Japanese terminology, Japan-specific distributions, and Japanese publication dates.
- Other official regional sources are compared against the Japanese baseline and are not assumed to represent distinct game binaries unless that identity is independently established.
- Public reverse-engineering projects are valuable technical evidence, but claims imported from them remain **Unverified / external evidence** in this repository until independently confirmed against a target build, extracted data, or another reproducible primary source.
- Publication-date differences caused by time zones are recorded as regional metadata and must not be treated as binary differences without further evidence.
- Unknown hashes, title revisions, internal build identifiers, and regional binary relationships remain `TBD` rather than being guessed.

## Official Japanese baseline sources

| ID | Source | Coverage | Current use |
| --- | --- | --- | --- |
| `OFF-JP-LINEUP-001` | https://www.pokemon.co.jp/ex/sword_shield/lineup/190605_01.html | Japanese official product lineup | Release date, publisher/developer roles, package/download forms, supported languages, Japanese baseline product metadata |
| `OFF-JP-UPD-110` | https://www.pokemon.co.jp/info/2020/01/200109_at01.html | Update Ver.1.1.0 | Japanese release chronology and change summary |
| `OFF-JP-UPD-111` | https://www.pokemon.co.jp/info/2020/03/200318_at01.html | Update Ver.1.1.1; also repeats Ver.1.1.0 | Japanese release chronology and change summary |
| `OFF-JP-UPD-120` | https://www.pokemon.co.jp/info/2020/06/200617_at01.html | Update Ver.1.2.0 | Isle of Armor-era update chronology and change summary |
| `OFF-JP-UPD-121` | https://www.pokemon.co.jp/info/2020/07/200708_at01.html | Update Ver.1.2.1 | Japanese release chronology and change summary |
| `OFF-JP-UPD-130` | https://www.pokemon.co.jp/info/2020/10/201023_at01.html | Update Ver.1.3.0 | Crown Tundra-era update chronology and change summary |
| `OFF-JP-UPD-131` | https://www.pokemon.co.jp/info/2020/12/201222_at01.html | Update Ver.1.3.1 | Japanese release chronology and change summary |
| `OFF-JP-UPD-132` | https://www.pokemon.co.jp/info/2021/05/210512_at01.html | Update Ver.1.3.2 | Final listed Sword/Shield update and change summary |
| `OFF-JP-NEWS-INDEX` | https://www.pokemon.co.jp/ex/sword_shield/news/?category=information | Japanese official news index | Discovery index for updates, distributions, raids, campaigns, and online notices |

## Official regional comparison sources

| ID | Source | Region / storefront | Current use |
| --- | --- | --- | --- |
| `OFF-NA-UPDATES` | https://en-americas-support.nintendo.com/app/answers/detail/a_id/48550/p/989/c/120 | Nintendo of America support | Regional update chronology and English change summaries |
| `OFF-US-SWORD` | https://www.nintendo.com/us/store/products/pokemon-sword-110262/ | United States | Supported languages, release date, SKU/UPC, DLC storefront metadata |
| `OFF-UK-SHIELD` | https://www.nintendo.com/en-gb/Games/Nintendo-Switch-games/Pokemon-Shield-1522110.html | United Kingdom / Europe | Supported languages, package/download product metadata, PEGI-facing storefront metadata |
| `OFF-AU-SHIELD` | https://www.nintendo.com/au/games/nintendo-switch/pokemon-shield/ | Australia | Supported languages, file-size/storefront metadata, regional product presentation |
| `OFF-NINTENDO-REGIONS` | https://www.nintendo.com/region-selector/ | Nintendo global region selector | Discovery map for official regional storefront/support sources |

## Public reverse-engineering and technical sources

| ID | Source | Type | Relevant evidence | Repository status |
| --- | --- | --- | --- | --- |
| `RE-PKNX` | https://github.com/kwsch/pkNX | Public reverse-engineering/editor source | Sword/Shield file mappings, localized message paths, PML data, encounter, raid, placement, shop, rental, Battle Tower and other mapped resources | External evidence; not independently target-verified |
| `RE-PKNX-MAPPING` | https://github.com/kwsch/pkNX/blob/master/pkNX.Game/File/GameFileMapping.cs | Source file | Maps `bin/message/*`, `bin/pml/*`, encounter tables, `data_table.gfpak`, `placement.gfpak`, shops and other paths | External evidence; not independently target-verified |
| `RE-PKHEX` | https://github.com/kwsch/PKHeX | Public save-format/editor source | Generation VIII save, PK8, legality, encounter and related data structures | External evidence; not independently target-verified |
| `RE-PKHEX-SAV8` | https://github.com/kwsch/PKHeX/blob/master/PKHeX.Core/Saves/SAV8SWSH.cs | Source file | `SAV8SWSH` Generation VIII Sword/Shield save object | External evidence; not independently target-verified |
| `RE-SWITCH-TOOLBOX` | https://github.com/KillzXGaming/Switch-Toolbox/wiki/Pokemon-Let%27s-Go-%26-Sword-Shield-%3A-Model-Importing | Public format/tool documentation | Reports `.gfbmdl` models and `.gfpak` archives used by Sword/Shield workflows | External evidence; not independently target-verified |
| `RE-HACTOOL` | https://github.com/SciresM/hactool | Public Nintendo Switch container tool | NCA, ExeFS, RomFS, NSO0 and related Switch container/file-system research context | Platform-level reference; no Sword-specific target verification |
| `DB-PROJECTPOKEMON-EVENTS` | https://projectpokemon.org/home/files/category/2-event-gallery/ | Community event archive | Mystery Gift / Wonder Card discovery and cross-check source for Generation VIII distributions | Secondary archive; individual events require provenance review |

## Confirmed public facts recorded in this batch

### Japanese product baseline

The Japanese official product page states a release date of **2019-11-15**, Nintendo Switch as the platform, package and download distribution, and nine supported languages: Japanese, English, Spanish, French, German, Italian, Korean, Traditional Chinese, and Simplified Chinese.

This establishes a multilingual software baseline, but it does **not** by itself prove that every retail region uses byte-identical program/content data. Regional binary identity remains `TBD`.

### Official update sequence

The Japanese official sources currently establish this update sequence:

| Version | Japanese official distribution date | Major publicly stated change |
| --- | --- | --- |
| 1.1.0 | 2020-01-10 | Expansion Pass purchase entry point, new Wedgehurst Station event, fixes |
| 1.1.1 | 2020-03-18 | Handling for problems caused by tampered Pokémon data, additional fixes |
| 1.2.0 | 2020-06-17 | The Isle of Armor support and additional Pokémon |
| 1.2.1 | 2020-07-08 | Link-code/password matching bug fix and additional fixes |
| 1.3.0 | 2020-10-23 | The Crown Tundra support and additional Pokémon |
| 1.3.1 | 2020-12-22 | Bug fixes |
| 1.3.2 | 2021-05-12 | Fix for some Pokémon icons in communication battles and additional fixes |

Nintendo of America lists corresponding dates as 2020-01-09, 2020-03-17, 2020-06-16, 2020-07-07, 2020-10-22, 2020-12-21, and 2021-05-11. At this stage this is recorded as a **regional publication/date presentation difference**, not evidence of different binaries.

### Publicly documented internal message-language layout

`kwsch/pkNX` currently maps Sword/Shield common and script message resources under language-specific paths including `JPN`, `JPN_KANJI`, `English`, `French`, `Italian`, `German`, `Spanish`, `Korean`, `Simp_Chinese`, and `Trad_Chinese`, with an unused language index noted in the mapping source.

Because this finding is imported from a public reverse-engineering project and this repository has no target dump, it remains **Unverified / external evidence** here. It is nevertheless a high-priority lead for the later language and regional comparison map.

## Coverage gaps opened by this batch

- Exact launch-build version identifier and hashes: `TBD`.
- Sword Title ID / content IDs / NCA identities from an authoritative or independently reproducible source: `TBD`.
- Whether Japan, Korea, North America, Europe, Hong Kong/Taiwan, Australia/New Zealand, and other storefront regions use byte-identical base/update content: `TBD`.
- Physical game-card revisions and later cartridges containing bundled updates: `TBD`.
- Region-specific packaging, ratings, SKU/UPC/JAN codes, and cartridge-label revisions: partial; requires systematic regional inventory.
- Korean, Hong Kong, Taiwan, continental Europe, Canada, Latin America, and other official regional pages: discovery in progress.
- Complete official Japanese distribution / raid / competition / online-service chronology: discovery in progress.
- Archived or removed official pages: not yet systematically enumerated.

## Next research batch

Continue Phase 0 by expanding official regional coverage and establishing a machine-readable version/region/language matrix. After that, begin the public technical file-map inventory from `pkNX`, PKHeX, Switch-Toolbox, and other independently discoverable sources while preserving source provenance and confidence levels.

_Last surveyed: 2026-09-14._
