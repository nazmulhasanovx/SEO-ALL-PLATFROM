# BinGi Structured Data Mapping — Technical Specification
**Date:** 2026-11-09

| Page | Candidate type | When to use | Caveats |
|---|---|---|---|
| Official brand overview | Organization (or WebSite) | Consistent organization/brand entity | Verify organization name, official URL and social accounts |
| Main HMS product | SoftwareApplication | Actual software product description | Eligibility and required/recommended fields vary; no false aggregateRating |
| Product/module breadcrumb | BreadcrumbList | Matching real visible hierarchy | Actual reachable URLs only |
| Editorial guide/article | Article / BlogPosting | True authored editorial page | Accurate author/publisher/datePublished/dateModified |
| FAQ content | Plain visible FAQs (optional FAQPage schema only where appropriate) | Real on-page questions | Google FAQ rich results primarily restricted to qualified authoritative government/health sites |
| Hotel property marketplace detail | LodgingBusiness or suitable hospitality type | Only real verified property listing | Exact name, address, contact, price and booking policy verified |
| Review | Review / AggregateRating | Only when truly eligible and based on genuine review evidence | No self-serving/fake review claims; follow engine policies |

There is no special "GEO" schema that forces AI results. Many schema.org types are valid vocabulary but do not receive Google-specific rich results. Structured data is not a substitute for visible helpful content.

## Rules
- JSON-LD mirrors visible copy; keep one clear entity ID when appropriate.
- Avoid defining multiple conflicting organizations/products across site versions.
- Public website is different from authenticated hotel dashboard.
- Verify plan/offer data against the live approved pricing page before using Offer.
- Do not claim cross-platform/OS support without release evidence.
- Update schema when any page content, URL or plan changes.

## Authoritative references
https://developers.google.com/search/docs/appearance/structured-data
https://developers.google.com/search/docs/appearance/structured-data/software-app
https://developers.google.com/search/docs/appearance/structured-data/sd-policies
https://developers.google.com/search/blog/2023/08/howto-faq-changes
