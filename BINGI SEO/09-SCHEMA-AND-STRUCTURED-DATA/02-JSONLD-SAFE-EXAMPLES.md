# JSON-LD Examples — Do Not Publish Without Validation
**Templates only. No false pricing, rating, reviews or promises.**

## A. Official organization on B2B homepage
```json
{
  "@context": "https://schema.org",
  "@type": "Organization",
  "@id": "https://technology.bingi.com.bd/#organization",
  "name": "BinGi",
  "url": "https://technology.bingi.com.bd/"
}
```
**Review:** BinGi may be a brand rather than a separately registered organization. If the legally correct entity is NEONECY, model its relationship accurately using appropriate schema types after owner/legal sign-off. Example shown for illustration.

## B. Breadcrumb on existing hotels solution
```json
{
  "@context": "https://schema.org",
  "@type": "BreadcrumbList",
  "itemListElement": [
    {"@type": "ListItem", "position": 1, "name": "BinGi", "item": "https://technology.bingi.com.bd/"},
    {"@type": "ListItem", "position": 2, "name": "Hotels", "item": "https://technology.bingi.com.bd/solutions/hotels"}
  ]
}
```
Only deploy if that is the real navigational hierarchy shown on the page.

## C. SoftwareApplication — field strategy, not invented full object
```text
@type: SoftwareApplication
name: Exact approved public product name
url: Official canonical product page
description: Visible description, plan-limited if relevant
applicationCategory: Verified software category
operatingSystem: Include only if verified
offers: Include only current publicly offered real pricing
aggregateRating: OMIT unless real eligible ratings exist
```

Google software app rich result eligibility has requirements and policy constraints; verify current docs and exact real offering before constructing markup. Do not insert an invented zero-price offer to satisfy validators.

## D. Blog article
Include `headline`, `datePublished`, `dateModified`, `author` and `publisher` only as factually supported by the visible article metadata.

## Validation
Check with Google's Rich Results Test and Schema Markup Validator; inspect rendered page, not just pre-production text.
