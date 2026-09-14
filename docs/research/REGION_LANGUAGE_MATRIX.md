# Region and Language Evidence Matrix

This document tracks public evidence for **Pocket Monsters Sword / Pokémon Sword** regional sales, storefronts, packaging-facing metadata, supported languages, ratings, and release presentation.

The Japanese release is the comparison baseline. A regional storefront or package listing is **not** evidence of a distinct executable, RomFS, NCA, or game-card revision. Binary/content identity remains unresolved until independently established.

## Interpretation rules

- `Sales/storefront confirmed` means an official regional Nintendo or Pokémon source has been located.
- `Language list` records what that specific official source states; a shortened European label such as `Chinese` must not automatically be expanded into Simplified + Traditional unless another source does so explicitly.
- `Binary identity` remains `TBD` unless hash/content identity is independently established.
- Ratings, SKU/UPC/JAN codes, price, packaging, local publisher/distributor wording, and publication dates are regional metadata worth preserving even when software content later proves identical.
- Region and language are separate axes. A Korean storefront does not imply a Korean-only binary, and Japanese baseline software officially supports multiple languages.

## Current matrix

| Region / market | Official public source | Release evidence | Language evidence from that source | Regional metadata | Binary identity |
| --- | --- | --- | --- | --- | --- |
| Japan | https://www.pokemon.co.jp/ex/sword_shield/lineup/190605_01.html | 2019-11-15 | Japanese, English, Spanish, French, German, Italian, Korean, Traditional Chinese, Simplified Chinese | CERO A; package/download; Pokémon publisher, Nintendo sales, GAME FREAK development | TBD — baseline |
| Korea | https://www.nintendo.com/kr/switch/sword_shield/ | 2019-11-15 | Detailed language list not captured on this page; Korean is confirmed among the JP baseline product's supported languages | KR retail price ₩64,800 each; Double Pack ₩129,600; Korean update-news chronology present | TBD |
| Korea | https://pokemonkorea.co.kr/game/view/5262?cate2=7&sword= | 2019-11 (month shown) | Korean localized product page | Publisher/distributor shown as 한국닌텐도(주) | TBD |
| United States | https://www.nintendo.com/us/store/products/pokemon-sword-110262/ | 2019-11-15 | Japanese, French, German, Italian, Spanish, Korean, Simplified Chinese, Traditional Chinese, American English | ESRB; SKU 110262; UPC 00045496596583 | TBD |
| Canada — English | https://www.nintendo.com/en-ca/store/products/pokemon-sword-switch/ | 2019-11-15 | Japanese, French, German, Italian, Spanish, Korean, Simplified Chinese, Traditional Chinese, American English | Canadian storefront; DLC pricing differs from US storefront | TBD |
| Canada — French | https://www.nintendo.com/fr-ca/store/products/pokemon-sword-switch/ | 2019-11-15 | Same nine-language list presented in French | French Canadian storefront presentation; ESRB | TBD |
| United Kingdom | https://www.nintendo.com/en-gb/Games/Nintendo-Switch-games/Pokemon-Sword-1522111.html | 2019-11-15 | Japanese, English, Spanish, French, German, Italian, Korean, Chinese | PEGI 7; game card and download version listed; 12.4 GB download size | TBD |
| Germany | https://www.nintendo.com/de-de/Spiele/Nintendo-Switch-Spiele/Pokemon-Schild-1522110.html | 2019-11-15 (Shield comparison page) | Japanese, English, Spanish, French, German, Italian, Korean, Chinese | USK 6; game card and download metadata | TBD; Shield page used only as ecosystem/regional presentation reference pending Sword-specific capture |
| Spain | https://www.nintendo.com/es-es/Juegos/Juegos-de-Nintendo-Switch/Pokemon-Espada-1522111.html | 2019-11-15 | Japanese, English, Spanish, French, German, Italian, Korean, Chinese | PEGI 7; Spanish title `Pokémon Espada` | TBD |
| France | https://www.nintendo.com/fr-fr/Jeux/Jeux-Nintendo-Switch/Pokemon-Bouclier-1522110.html | 2019-11-15 (Shield comparison page) | Japanese, English, Spanish, French, German, Italian, Korean, Chinese | PEGI 7; French Shield title `Pokémon Bouclier` | TBD; Shield page used only as regional ecosystem reference pending Sword-specific capture |
| Netherlands | https://www.nintendo.com/nl-nl/Games/Nintendo-Switch-games/Pokemon-Sword-1522111.html | 2019-11-15 | Japanese, English, Spanish, French, German, Italian, Korean, Chinese | PEGI 7; 12.4 GB | TBD |
| Belgium | https://www.nintendo.com/nl-be/Games/Nintendo-Switch-games/Pokemon-Sword-1522111.html | 2019-11-15 | Japanese, English, Spanish, French, German, Italian, Korean, Chinese | PEGI 7 | TBD |
| Portugal | https://www.nintendo.com/pt-pt/Jogos/Jogos-para-a-Nintendo-Switch/Pokemon-Sword-1522111.html | 2019-11-15 | Japanese, English, Spanish, French, German, Italian, Korean, Chinese | PEGI 7 | TBD |
| Australia | https://www.nintendo.com/au/games/nintendo-switch/pokemon-sword/ | 2019-11-15 | Japanese, English, French, German, Italian, Spanish, Korean, Simplified Chinese, Traditional Chinese | 12.4 GB; Save Data Cloud not supported; Australian rating presentation | TBD |
| Brazil | https://www.nintendo.com/pt-br/store/products/pokemon-sword-switch/ | 2019-11-15 | Japanese, French, German, Italian, Spanish, Korean, Simplified Chinese, Traditional Chinese, American English | Portuguese Brazilian storefront; regional DLC pricing/presentation | TBD |
| Hong Kong | https://store.nintendo.com.hk/download-code | Regional sale presence confirmed | Detailed Sword-specific language list not yet captured | Official HK store currently lists `寶可夢 劍` and `寶可夢 盾` download codes; observed price HKD 329 at survey time | TBD |
| Taiwan | TBD | Official Sword-specific product source not yet captured in this batch | TBD | Nintendo Taiwan/HK historical and support sources require further discovery | TBD |
| New Zealand | TBD | Separate NZ Sword product page not yet captured in this batch | TBD | Australia/NZ regional relationship must not be assumed | TBD |
| Mexico / Spanish-speaking Americas | TBD | Nintendo global region selector confirms regional sites, but Sword-specific official page not yet catalogued | TBD | Requires country-by-country storefront/support survey | TBD |
| Argentina / Chile / Colombia / Peru | TBD | Regional Nintendo sites exist; Sword-specific evidence not yet catalogued | TBD | Requires country-by-country survey | TBD |
| Other EMEA Nintendo markets | Partial | Multiple European country pages share Nintendo Europe product infrastructure | Usually the same eight displayed language categories on captured pages | Country-specific ratings/storefront/presentation may differ | TBD |

## Cross-region observations from current official pages

1. Japan, the United States, Canada, the United Kingdom, several European country pages, Australia, Brazil, and Korea all publicly anchor the launch to **2019-11-15** (the Pokémon Korea catalogue page gives only November 2019, while Nintendo Korea gives the exact date).
2. The Japanese, US/Canadian, and Australian pages explicitly distinguish **Simplified Chinese** and **Traditional Chinese**. Captured Nintendo Europe pages commonly display a single `Chinese` language label; this is a presentation difference and should not be over-interpreted as a software-content difference.
3. US product metadata exposes SKU/UPC identifiers; European pages emphasize PEGI/local ratings and package/download forms; Korea exposes local retail pricing; Australia explicitly states Save Data Cloud is unsupported. These are regional metadata differences even before binary comparison is possible.
4. Official Japanese, Korean, and North American update pages use local calendar dates. Some corresponding update dates differ by one day between Japan/Korea and North America; this is currently treated as timezone/publication metadata, not a distinct update build.

## Region-vs-language research requirement

The final survey must maintain at least two linked tables:

- **Market/region table:** sales territory, official storefront/support site, package identifiers, rating authority, local publisher/distributor, price/currency, release/update publication dates, physical revisions, and distribution campaigns.
- **Language table:** Japanese (including internal kana/kanji message-bank questions), English, Spanish, French, German, Italian, Korean, Simplified Chinese, Traditional Chinese, plus any internal unused/reserved language slots reported by technical sources.

The two tables must not be collapsed into a single concept of “regional ROM.”

## High-priority gaps

- Locate Sword-specific official Hong Kong product details and any Taiwan-localized product/support pages.
- Catalogue Nintendo Korea update-detail pages individually rather than only the news index.
- Capture New Zealand and remaining Americas storefront pages.
- Enumerate all Nintendo Europe country/local-language storefront variants and ratings.
- Catalogue physical package identifiers (JAN/EAN/UPC/product codes) and game-card label/revision evidence from provenance-bearing public sources.
- Determine whether public CDN/eShop metadata can establish shared or distinct Title IDs/content identities without relying on redistributed game binaries.
- Do not mark any regional targets `Verified` until identity/hashes meet `VERIFICATION.md` requirements.

_Last surveyed: 2026-09-14._
