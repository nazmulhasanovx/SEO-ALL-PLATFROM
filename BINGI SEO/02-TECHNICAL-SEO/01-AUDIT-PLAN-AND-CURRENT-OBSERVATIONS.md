# Crawl / Indexing / Technical SEO — Audit Workbook
**Initial document:** 2026-11-09 | **Audit status:** PENDING ACCESS

## Scope
Primary host: `technology.bingi.com.bd` — B2B landing pages, product, modules, blog, guides, pricing.
Separate host: `bingi.com.bd` — B2C property and destination pages.

## Limited publicly observable facts
At the time of drafting, public search results showed discoverable pages on the B2B domain including:
- https://technology.bingi.com.bd/
- https://technology.bingi.com.bd/pricing
- https://technology.bingi.com.bd/ecosystem
- https://technology.bingi.com.bd/solutions/hotels
- https://technology.bingi.com.bd/blog/hotel-management-software-budget-bangladesh

This does NOT prove completeness of indexing, which URLs are canonical, valid sitemap availability, crawler accessibility, or performance. Pricing was observed in a newer structure (Free Trial / Online / Business / Complete and higher tiers in the comparison flow); verify owner-approved terms.

## Collect before diagnosing
- Google Search Console verified property access for each host, coverage reports and sitemap details.
- Bing Webmaster Tools verification, IndexNow submission logs.
- Current site framework, deployment method, CDN, rewrites, robots.txt and sitemap generation.
- Existing URL inventory and server logs; production/staging distinction.
- Page-level HTML response, mobile rendering, status codes, canonicals and hreflang.
- GA4/analytics, demo-request conversion configuration and privacy controls.

## Audit matrix — record evidence in a new results file
| Check | Method | Evidence to save | Severity if broken |
|---|---|---|---|
| 200 status for priority URLs | HTTP HEAD+GET and rendered page | URL/status/date | P0 |
| robots.txt per host | Fetch actual endpoint and parse | URL/directives/date | P0 |
| Meta robots / X-Robots-Tag | Inspect HTML + headers | page and response | P0 |
| Sitemap exists / valid / canonical | Fetch XML + URL inspection | URL count and errors | P0 |
| Canonical points correctly | Inspect canonical, redirects | URL pairing | P0 |
| HTML content accessible | Fetch source with JS off | H1/body/navigation | P0 |
| Mobile parity | mobile screenshot + rendered HTML | missing links/content | P1 |
| Titles & descriptions | crawl all public indexable pages | duplication report | P1 |
| Language alternates | inspect pairs + reciprocal tags | EN↔BN matrix | P1 |
| Page speed / LCP INP CLS | PageSpeed + CrUX or lab | date + metrics | P1/P2 |
| Structured data validation | Rich Results Test + Schema validator | warnings/errors | P2 |
| Broken links/redirect chains | crawled graph | source/target/response | P1 |
| Private dashboards | logged-out inspection, auth checks | URL path policy | P0 |
| 404/soft 404 and filters | crawl query variants | status and canonical | P1 |

## Severity
- **P0:** Blocks crawl/indexing or leaks private data.
- **P1:** Damages priority organic coverage or user conversion.
- **P2:** Quality/performance enhancement.

## Result template
`AUDIT-YYYYMMDD-ID | host | URL | issue | actual | expected | evidence | severity | owner | fix PR | verified date`.

Do NOT fill the matrix with PASS or FAIL without accessing the actual URLs/tool reports.
