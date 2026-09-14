# Project Pokémon Generation VIII Event Archive Survey

Project Pokémon is treated here as a **secondary/community archival and reverse-engineering source**, not as a substitute for official provenance. Its Generation VIII gallery is nevertheless a major technical corpus because it preserves Wonder Card/event records and metadata that official campaign prose often does not expose.

## Current category counts observed

The Event Gallery currently reports:

- Generation VIII total: **243**
- Sword & Shield: **215**
- Brilliant Diamond & Shining Pearl: **14**
- Legends: Arceus: **14**

These counts are discovery anchors and can change as the archive is maintained. They must therefore be recorded with a survey date rather than treated as immutable game facts.

## Generation VIII format notes recorded by the archive

The Generation VIII category states that:

- Switch titles can distribute Wonder Cards tied to more than one language, so the category is not divided into the older language-localized structure;
- Nintendo Switch is region-free, so console region itself is not a redemption factor;
- individual local events can still contain Japanese-only or otherwise language-specific descriptions, OT names, nicknames or metadata;
- `.wc8`, `.wb8` and `.wa8` Wonder Cards are not stored directly in the save for Sword/Shield, BDSP or Legends: Arceus;
- public tooling can use the files to construct gift Pokémon, while BCAT-based workflows are relevant to claiming network-delivered gifts.

These are **external technical claims** in this repository and remain subject to independent cross-checking.

## Sword/Shield archive scope

The Sword/Shield subcategory currently contains **215 files**. The archive mixes multiple materially different research classes that must be split during enumeration:

- Pokémon Mystery Gifts;
- serial-code distributions;
- local Pokémon Center distributions;
- item/clothing gifts;
- Wild Area News / raid-event data;
- event revisions or replacements;
- regional variants;
- language-dependent metadata;
- files whose public archive entry documents a distribution that official pages no longer describe in technical detail.

The 215 count must therefore **not** be equated to 215 unique Pokémon distributions.

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

The archive also preserves individual Wild Area event packages and technical observations. These records can expose event-pool indices, encounter rates, abilities, catch rates, IV settings, moves, shield parameters and other data not present in official news prose.

Such fields are high-value reverse-engineering leads but remain **external evidence** until corroborated.

## Required enumeration work

For all **215 Sword/Shield archive records**, capture at least:

- Project Pokémon file-entry ID and URL;
- archive title;
- event class;
- submitted/published/updated dates;
- distribution dates stated by the archive;
- region/campaign provenance;
- WC8/BCAT/Wild Area data class;
- Wonder Card ID where provided;
- language slots and language-dependent differences;
- Pokémon/item/raid contents;
- revision/replacement history;
- link to the corresponding official source when found;
- whether the archive record is released, unreleased, beta, superseded or uncertain;
- verification/cross-check status.

## Completion rule

Project Pokémon is not `Reviewed` until all 215 Sword/Shield entries have individual records and have been classified. It is not `Cross-checked` until each record with a traceable official campaign has been connected to that primary evidence or explicitly marked as lacking a surviving primary source.

**Status: Enumerating — not complete.**

Sources surveyed: Project Pokémon Event Gallery, Generation VIII category, Sword & Shield category, and selected event/unreleased entries.

_Last updated: 2026-09-14._
