# Technical Implementation — Indexability, Canonicals & XML Sitemaps
**Status:** SPECIFICATION ONLY (not deployed)

## Publication rules
Only public, canonical, 200-status, indexable pages with real helpful content go in sitemaps. Keep booking confirmations, search/filter parameter permutations, accounts, checkouts, guest identities and staff/private data out of indexing.

Do not assume a page is indexed just because it appears in XML. Verify actual status in Search Console/Bing.

## Canonical tags
Each primary language page has a self-canonical `<link rel="canonical" href="https://.../en/.../">` unless there is a deliberate alternate canonical decision. Do not canonicalize the Bangla translation to the English page—different language pages should generally self-canonicalize.

## Proposed sitemap partitioning
```text
technology.bingi.com.bd/sitemap.xml
  sitemap-main.xml
  sitemap-modules-en.xml
  sitemap-modules-bn.xml
  sitemap-solutions.xml
  sitemap-guides.xml
  sitemap-blog.xml
bingi.com.bd/sitemap.xml
  sitemap-destinations.xml
  sitemap-properties.xml
```
Names are **suggestions**, not confirmed live endpoints. An index can group appropriately and must be served at a valid location. Split as content grows.

## Sample XML (ILLUSTRATIVE — don't submit until these pages exist)
```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9"
 xmlns:xhtml="http://www.w3.org/1999/xhtml">
  <url>
    <loc>https://technology.bingi.com.bd/en/modules/reservations/</loc>
    <xhtml:link rel="alternate" hreflang="en" href="https://technology.bingi.com.bd/en/modules/reservations/"/>
    <xhtml:link rel="alternate" hreflang="bn" href="https://technology.bingi.com.bd/bn/modules/reservations/"/>
  </url>
  <url>
    <loc>https://technology.bingi.com.bd/bn/modules/reservations/</loc>
    <xhtml:link rel="alternate" hreflang="en" href="https://technology.bingi.com.bd/en/modules/reservations/"/>
    <xhtml:link rel="alternate" hreflang="bn" href="https://technology.bingi.com.bd/bn/modules/reservations/"/>
  </url>
</urlset>
```
Only include those URLs once live and indexable. Keep alternate links reciprocal for genuine equivalents.

## Migration safeguards
1. Export old URL list and organic landing-page performance.
2. Decide keep URL vs redirect; preserve existing high-value routes when possible.
3. Implement a single 301 from each superseded URL to the closest equivalent.
4. Replace old internal links and sitemap entries.
5. Update canonical and hreflang pointers to final destinations.
6. Confirm response code, rendered content, indexed canonical; re-check after migration.

## Sources
- https://developers.google.com/search/docs/crawling-indexing/sitemaps/build-sitemap
- https://developers.google.com/search/docs/specialty/international/localized-versions
