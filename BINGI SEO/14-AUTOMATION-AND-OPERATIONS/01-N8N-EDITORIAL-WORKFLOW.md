# n8n SEO Content Pipeline — Architecture Proposal
**State:** Proposed; not installed or scheduled.

## High-level workflow
```text
Approved Topic Backlog / Product Release Change
                   |
                   v
             SEO Research Brief
                   |
                   v
             English Content Draft
                   |
                   v
             Bangla Localization
                   |
                   v
       Source / Feature / Pricing Validator
                   |
                   v
       HUMAN APPROVAL REQUIRED? ------ NO ---> HOLD
                   |
                  YES
                   v
           Staging CMS Publish
                   |
                   v
       QA: pages, locale, links, metadata
                   |
                   v
         Final Release Authorization
                   |
                   v
          Production CMS Publish
                   |
                   v
       Sitemap Refresh / IndexNow if valid
                   |
                   v
       Search Console + Bing Monitoring
                   |
                   v
           Report / Improvement Queue
```

## Recommended nodes (conceptual)
1. Trigger: approved editorial task, release event or manual batch start.
2. Load: approved product fact sheet & module record from controlled source.
3. Retrieve: search-intent brief and existing URL to prevent duplicate pages.
4. Draft: English copy; annotate uncertain claims for reviewer.
5. Localize: বাংলা with glossary and exact feature parity.
6. Validation: require non-empty source IDs, plan/version scope, approved images.
7. Human gate: content owner and product fact reviewer approve signed-off revision.
8. Staging: create CMS draft only; never immediate production publish on first generation.
9. QA: HTTP checks, canonical/hreflang, links, schema validation, accessibility.
10. Publish: only if approval id matches content version.
11. Notify: sitemap/IndexNow for eligible published URLs, record submission response.
12. Monitor: errors, index trends and lead conversions; generate review tasks.

## n8n integration boundaries
- CMS credentials and webhooks belong in encrypted runtime secrets, **not GitHub or content files**.
- Use per-domain credentials with least privilege; no public token or API key exposure.
- Avoid publishing same language/slug twice with stable idempotency keys.
- No automatic publishing of claimed integrations, client testimonials or contract terms.

## Existing content adaptation
Import current blog/page inventory before generating new pages. Correct duplicate intent and outdated facts rather than mass-producing hundreds of posts.
