# Publishing Automation — Quality & Failure Cases

## Safety gates
- **Claim gate:** Product owner approves every new module, feature, pricing, OTA, hardware, AI or security claim.
- **Locale gate:** English and বাংলা equivalents have reviewer sign-off; do not publish incomplete languages and add bogus hreflang.
- **URL gate:** Unique canonical destination. Migration/redirects need separate approval.
- **Security gate:** No credentials, real guest data, staff PII, sensitive client documents or private commercial information in public drafts.
- **Live validation gate:** Page actually available on live domain with correct metadata before marking complete.

## Failure matrix
| Failure | Action |
|---|---|
| Missing verified product evidence | Hold and request owner review |
| Translation changes promise/price | Block both locales pending correction |
| CMS API unavailable | Retry safely with backoff; do not duplicate draft |
| URL collision | Stop auto-publish; compare existing page |
| Broken canonical / hreflang | Keep staging or roll back publication |
| Sitemap update fails | Record failure; run manual submission after page verification |
| IndexNow submission succeeds | Log as notified, not indexed |
| Product price changes | Flag affected pages and schema for coordinated updates |
| Client withdraws consent | Remove affected content after verifying scope and document archival/redirection |

## Publishing ledger
Fields: content_id, revision, en_url, bn_url, source_version, factual_approver, editorial_approver, publish_authorizer, CMS draft IDs, QA checks, deploy timestamp, rollback revision, last monitored.

## Critical operations
Have backups and a documented restore process. Log publishing events but redact sensitive content. Review automation output weekly in initial launch.
