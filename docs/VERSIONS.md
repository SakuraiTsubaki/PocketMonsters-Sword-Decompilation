# Version Coverage

Use this document as the authoritative inventory of game versions targeted by this decompilation project.

The project currently has **no locally owned retail game dump**, so public-source entries are recorded as **Reference only** until target identity and cryptographic hashes can be independently confirmed. The Japanese release is the comparison baseline; regional publication dates and metadata are preserved separately and are not assumed to imply distinct binaries.

| Status | Region | Language | Revision / update | Platform / build | Hashes | Notes |
| --- | --- | --- | --- | --- | --- | --- |
| Reference only | JP baseline | Official product supports 9 languages | Launch release; exact internal version TBD | Nintendo Switch | TBD | Released 2019-11-15. Package and download versions listed by the Japanese official product page. |
| Reference only | JP baseline | Binary language identity TBD | Ver. 1.1.0 | Nintendo Switch | TBD | JP official distribution date 2020-01-10. NA official support lists 2020-01-09; treat as regional publication/date metadata until binary identity is established. |
| Reference only | JP baseline | Binary language identity TBD | Ver. 1.1.1 | Nintendo Switch | TBD | JP 2020-03-18; NA 2020-03-17. |
| Reference only | JP baseline | Binary language identity TBD | Ver. 1.2.0 | Nintendo Switch | TBD | JP 2020-06-17; NA 2020-06-16. Isle of Armor support. |
| Reference only | JP baseline | Binary language identity TBD | Ver. 1.2.1 | Nintendo Switch | TBD | JP 2020-07-08; NA 2020-07-07. |
| Reference only | JP baseline | Binary language identity TBD | Ver. 1.3.0 | Nintendo Switch | TBD | JP 2020-10-23; NA 2020-10-22. Crown Tundra support. |
| Reference only | JP baseline | Binary language identity TBD | Ver. 1.3.1 | Nintendo Switch | TBD | JP 2020-12-22; NA 2020-12-21. |
| Reference only | JP baseline | Binary language identity TBD | Ver. 1.3.2 | Nintendo Switch | TBD | JP 2021-05-12; NA 2021-05-11. Latest official Sword/Shield update currently identified. |

## Officially supported languages at launch

The Japanese official product page lists:

- Japanese
- English
- Spanish
- French
- German
- Italian
- Korean
- Chinese (Traditional)
- Chinese (Simplified)

This confirms product-level language support. It does not yet establish whether every regional package/storefront uses byte-identical program or content data.

## Regional identity status

Regional software identity is currently unresolved. Japan is the research baseline, while North America, Europe, Korea, Hong Kong/Taiwan, Australia/New Zealand, and other official sales/support regions must be inventoried independently. Storefront SKU, packaging, rating, publication-date, and distribution differences should be recorded even if later research proves the underlying software content to be identical.

See `research/PUBLIC_SOURCE_INDEX.md` and `../manifests/public-sources.json` for current provenance.

## Status vocabulary
- **Planned** — intended for investigation but not yet verified.
- **Verified** — identity and hashes confirmed.
- **Mapped** — executable/data layout documented.
- **In progress** — active source reconstruction.
- **Matched** — reconstruction verified against the target.
- **Reference only** — used for comparison but not a reconstruction target.

## Recording rules
1. Record exact revision/update information whenever known.
2. Prefer cryptographic hashes over filenames as identity evidence.
3. Do not commit retail game images or console keys.
4. Record regional or language differences instead of assuming two releases are identical.
5. Link version-specific findings to relevant documentation or verification issues.
