# Locale Architecture / Hreflang Technical Plan
**State:** PROPOSAL — verify current site routing before deployment.

## Language strategy
- English: `en` (international English-facing audience).
- বাংলা: `bn` (Bangla language).
- Only use a regional code such as `bn-BD` when the content genuinely targets that regional variant; language alone is often sufficient.
- Future `hi`, `ar` etc. only when content is translated, maintained and supported commercially.
- Do not force redirect every user or crawler from an English URL based on IP or browser; maintain accessible locale links.

## Proposed route pairs
| Page | English | বাংলা |
|---|---|---|
| B2B home | /en/ | /bn/ |
| Reservations | /en/modules/reservations/ | /bn/modules/reservations/ |
| Housekeeping | /en/modules/housekeeping/ | /bn/modules/housekeeping/ |
| Resort solution | /en/solutions/resorts/ | /bn/solutions/resorts/ |

**Important:** Current public pages use routes like `/solutions/hotels`. Do not deploy these sample paths without content migration and redirect planning.

## Example head tags (illustrative; final URLs must exist)
```html
<link rel="canonical" href="https://technology.bingi.com.bd/en/modules/reservations/" />
<link rel="alternate" hreflang="en" href="https://technology.bingi.com.bd/en/modules/reservations/" />
<link rel="alternate" hreflang="bn" href="https://technology.bingi.com.bd/bn/modules/reservations/" />
```

On the Bangla equivalent, use its own Bangla canonical and the same complete reciprocal alternate set. If adding x-default, point it at a genuinely appropriate language selector or global default page; do not invent one.

## HTML language and navigation
English `<html lang="en">`, বাংলা `<html lang="bn">`. Accessible visible language switch with clear labels. Keep language links crawlable standard anchors. Canonical tags remain self-referential for distinct language translations.

## Translation parity
A translated page should reflect the same feature release, plan boundaries and last-reviewed facts. Publish no hreflang to a missing/unapproved page; avoid partial pages with placeholder translation.

## Sources
https://developers.google.com/search/docs/specialty/international/localized-versions
https://developers.google.com/search/docs/specialty/international/managing-multi-regional-sites
