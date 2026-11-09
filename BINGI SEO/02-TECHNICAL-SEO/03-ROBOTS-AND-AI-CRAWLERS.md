# Crawlers, Robots & AI Search — Domain Policy
**Version:** 1.0 | **Status:** REVIEW REQUIRED; no robots changes made

## Objective
Expose verified public marketing/docs while protecting private applications and guest/employee data. `robots.txt` is **not an access-control or privacy tool**: authentication and authorization must secure private pages/data.

## Robots review protocol
Inspect and save each host's actual `/robots.txt`, HTTP status, sitemap declarations and relevant `X-Robots-Tag` / page meta robots. Different subdomains need their own rules.

## Illustrative robots policy (NOT production-ready)
```text
User-agent: *
Allow: /
Sitemap: https://technology.bingi.com.bd/sitemap.xml
```
This is a starting illustration only. Engineering must confirm private paths, staging rules and crawler access. Do not block CSS/JS required to render public pages. Secure admin pages with real authentication; `noindex` may be a secondary signal but must not replace access controls.

## AI crawler separation
- **OAI-SearchBot:** OpenAI's search-oriented crawler. If BinGi chooses to be eligible for ChatGPT Search retrieval, review its crawl policy.
- **GPTBot:** separate from OAI-SearchBot; policy for use in model development/training may be chosen independently.
- **Googlebot / Bingbot:** key search crawlers; allow access to intended public content.
- Other bot user agents: verify each provider's current documentation before implementing policy.

Being crawlable makes discovery possible; it does not guarantee indexing, ranking, citations, or mention in an AI answer. Distinguish web search data retrieval from a model's internal training data.

## Security rule
Never include credential URLs, guest IDs, staff data, private reports, order/payment details or customer records in SEO pages, sitemaps or generated knowledge exports.

## Optional llms.txt
An `/llms.txt` document may offer an auxiliary human/agent-friendly index of authoritative pages, but there is no universal rule that search engines use it for ranking. Public crawlable HTML/docs remain primary.

## Sources
- https://platform.openai.com/docs/bots
- https://developers.google.com/search/docs/crawling-indexing/robots/intro
