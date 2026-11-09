# Site Engineering QA & Acceptance Tests
**Status:** Unexecuted test plan.

## Tests for every priority English/Bangla landing page
- [ ] URL loads 200 via desktop/mobile and unauthenticated browser.
- [ ] Main text and heading visible in rendered HTML and without essential JS interaction.
- [ ] No accidental `noindex`, robots disallow or X-Robots-Tag.
- [ ] Correct self-canonical, one useful H1, distinct title/description, descriptive internal anchor links.
- [ ] EN and BN equivalents linked visibly and with reciprocal hreflang.
- [ ] Images have alt text; screenshot is genuine and optimized; no layout shift.
- [ ] Structured data matches visible content and passes applicable validation.
- [ ] Sitemap only lists valid canonical public URLs, updated after publish.
- [ ] No guest/employee details in content, code, schema, sitemap or assets.
- [ ] Conversion CTA works, can be measured with consent-compliant analytics.
- [ ] No broken links, long redirect chains or mixed content.
- [ ] Mobile UX, Core Web Vitals and accessibility reviewed.

## Event tracking proposal (not installed)
`demo_request_submit`, `pricing_contact_submit`, `module_demo_click`, `organic_signup_complete`; dedupe and do not send personal details as analytics event parameters.

## Search monitoring
1. Create or validate Google Search Console and Bing Webmaster Tools properties.
2. Submit verified sitemap and inspect selected page URLs.
3. Investigate 'Crawled - currently not indexed', duplicate canonical and redirect issues based on real reports.
4. Optionally implement IndexNow for Bing/participating engines after verified ownership.
5. Remember URL submission does not promise indexing.

## Sources
- https://www.bing.com/webmasters/help/?topicid=62f2860b
- https://www.bing.com/indexnow/getstarted
- https://developers.google.com/search/docs/appearance/structured-data/sd-policies

## Handoff record
Responsible engineer: TBD; website release date: TBD; Search Console properties: TBD; actual issues: TBD; fix verification: TBD.
