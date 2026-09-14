# Project Pokémon Generation VIII Event Archive Survey

Project Pokémon is treated here as a **secondary/community archival and reverse-engineering source**, not as a substitute for official provenance. Its Generation VIII gallery is nevertheless a major technical corpus because it preserves Wonder Card/event records and metadata that official campaign prose often does not expose.

## Current category counts observed

The Event Gallery currently reports:

- Generation VIII total: **243**
- Sword & Shield: **215**
- Brilliant Diamond & Shining Pearl: **14**
- Legends: Arceus: **14**

These counts are discovery anchors and can change as the archive is maintained. They are recorded with a survey date rather than treated as immutable game facts.

## Sword/Shield title census — 215 / 215 indexed

The Sword/Shield category spans nine pages. Every currently listed title has now been enumerated into repository manifests:

| Page | Entries | Manifest |
| --- | ---: | --- |
| 1 | 25 | `manifests/project-pokemon-swsh-page-01.json` |
| 2 | 25 | `manifests/project-pokemon-swsh-page-02.json` |
| 3 | 25 | `manifests/project-pokemon-swsh-page-03.json` |
| 4 | 25 | `manifests/project-pokemon-swsh-page-04.json` |
| 5 | 25 | `manifests/project-pokemon-swsh-page-05.json` |
| 6 | 25 | `manifests/project-pokemon-swsh-page-06.json` |
| 7 | 25 | `manifests/project-pokemon-swsh-page-07.json` |
| 8 | 25 | `manifests/project-pokemon-swsh-page-08.json` |
| 9 | 15 | `manifests/project-pokemon-swsh-page-09.json` |
| **Total** | **215** | `manifests/project-pokemon-swsh-index.json` |

The arithmetic check is `25 × 8 + 15 = 215`.

This completes the **title-level census only**. It does not mean that all 215 records have been content-reviewed or connected to primary sources.

## Generation VIII format notes recorded by the archive

The Generation VIII category states that:

- Switch titles can distribute Wonder Cards tied to more than one language, so the category is not divided into the older language-localized structure;
- Nintendo Switch is region-free, so console region itself is not a redemption factor;
- individual local events can still contain Japanese-only or otherwise language-specific descriptions, OT names, nicknames or metadata;
- `.wc8`, `.wb8` and `.wa8` Wonder Cards are not stored directly in the save for Sword/Shield, BDSP or Legends: Arceus;
- public tooling can use the files to construct gift Pokémon, while BCAT-based workflows are relevant to claiming network-delivered gifts.

These are **external technical claims** in this repository and remain subject to independent cross-checking.

## Data classes found in the 215-record census

The archive is not simply a list of 215 event Pokémon. The title census contains at least:

- Pokémon distributions;
- item distributions;
- clothing distributions;
- Dynamax Crystal distributions;
- competition participation rewards;
- Ranked Battle rewards;
- Wild Area News / Max Raid event packages;
- Wild Area base-state data;
- Wild Area event revision chains;
- downloadable competition-rule data;
- HOME-linked distributions;
- movie/anime tie-ins;
- local-wireless events;
- retailer/product bonuses;
- regional variants and region-dependent redemption behavior.

The 215 count must therefore **not** be equated to 215 unique Pokémon distributions or 215 independent technical event identities.

## High-priority revision / error evidence identified during the census

The title/category review already surfaced several cases that require dedicated historical preservation rather than normalization:

- **Wild Area Event #20: July 2020** — archive documents multiple redistributed indices, including a crash-causing reward item, incomplete fixes, server/online issues and a later proper fix. A missing intermediate index is explicitly noted by the archive.
- **Wild Area Event #14: May 2020** — archive reports a Shield 1-star Drilbur with Hydro Pump, corrected roughly nine hours later.
- **Wild Area Event #64: Urshifu Challenge** — archive reports an erroneous shiny Urshifu event state followed by a correction.
- **Wild Area Event #51: Summer Ghost Event 2021** — archive notes partial file replacement while some files retained prior-index data.
- **Japanese Birthday Pikachu / Eevee** — archive records a PID behavior change beginning 2020-02-12.
- **Japanese Birthday Milcery** — archive records a Set Nickname Wonder Card revision beginning 2020-11-06.
- **WCS22 Sinistea** — archive records a Wonder Card gender-field programming error, while the legitimately received Pokémon is correctly genderless.
- **Ash's Dracovish** — archive records a male gender field error in the Wonder Card, while the legitimately received Pokémon is genderless.
- **International shiny Zacian / Zamazenta** — archive reports that Korean-issued serial codes could be redeemed on either Sword or Shield, while other international code sources were server-restricted to the opposite-version gift even though the underlying Wonder Card allowed both games.
- **Wild Area Event #00** — archive describes a near-null pre-Wild-Area-News baseline state despite the underlying file-index observations.

All of these remain external archive evidence until primary or independently reproducible corroboration is attached.

## Example cross-check: Japanese Birthday Pikachu

The archive's Japanese Birthday Pikachu record supplies internal fields absent from the Japanese campaign announcement, including a Wonder Card ID, TID, level, nature/ability/moves and a documented PID behavior change beginning on 2020-02-12.

Research method for this project:

1. use the official Japanese birthday page for campaign provenance, eligibility and period;
2. use the Project Pokémon record for candidate WC8/internal fields;
3. look for independent technical evidence or revision history where practical;
4. record any discrepancy instead of silently merging the two descriptions.

## Example unused/replaced evidence

The Project Pokémon unreleased/beta gallery contains an **unreleased Singapore Birthday Milcery version** that was reportedly replaced shortly before store opening, with changes involving the Set Nickname flag and OT language. This belongs in the project's unused/replaced-distribution research, not in the ordinary released-event list.

This example shows why the exhaustive survey must cover both the ordinary Generation VIII Event Gallery and the unreleased/beta gallery.

## Wild Area event evidence

The archive preserves individual Wild Area event packages and technical observations. These records can expose event-pool indices, encounter rates, abilities, catch rates, IV settings, moves, shield parameters, partial updates and correction chains that do not appear in official news prose.

Wild Area events must therefore be modeled as **versioned event-data states**, not merely as one row per public event name.

Such fields are high-value reverse-engineering leads but remain **external evidence** until corroborated.

## Required second-pass work for all 215 records

For every record, still capture and verify:

- direct Project Pokémon file-entry URL and file-entry identifier;
- archive title;
- event class;
- submitted/published/updated dates;
- distribution dates stated by the archive;
- region/campaign provenance;
- WC8/BCAT/Wild Area data class;
- Wonder Card ID where provided;
- language slots and language-dependent differences;
- Pokémon/item/clothing/raid/rules contents;
- revision/replacement history;
- link to corresponding official Japanese and regional sources when found;
- released, unreleased, beta, superseded, corrected or uncertain state;
- verification/cross-check status;
- deduplicated technical identity where one Wonder Card or event-data package was reused by multiple campaigns/regions.

## Completion rule

- **Indexed:** all 215 current Sword/Shield category titles have individual manifest records. **This milestone is complete.**
- **Reviewed:** every one of the 215 entries has a resolved direct archive record and structured content review. **Not complete.**
- **Cross-checked:** each traceable record is connected to surviving primary official evidence, or explicitly marked as lacking surviving primary provenance. **Not complete.**
- **Exhausted:** ordinary gallery, unreleased/beta/superseded records, technical discussion threads, BCAT/Wild Area event revisions and archive history have all been searched and reconciled. **Not complete.**

**Status: Indexed — 215 / 215 title census complete; detailed review continues.**

Sources surveyed: Project Pokémon Event Gallery, Generation VIII category, all nine Sword & Shield category pages, and selected event/unreleased entries.

_Last updated: 2026-09-14._
