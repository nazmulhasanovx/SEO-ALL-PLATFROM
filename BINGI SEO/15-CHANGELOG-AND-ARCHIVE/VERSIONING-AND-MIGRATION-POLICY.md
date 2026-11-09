# Documentation Versioning & Safe Migration Policy
**v1.0 | 2026-11-09 | Proposed**

## Safety rules
1. **Do not delete** old module/category source information just because a new design, copy or SEO plan is adopted.
2. Use Git commit history for every change; note the reason, affected module and dependencies.
3. For substantial rewrites, snapshot old content into `15-CHANGELOG-AND-ARCHIVE/ARCHIVE/YYYY-MM-DD/...` if a readable frozen copy is useful in addition to Git history.
4. Archive copies must be clearly marked superseded and not mistaken for current publishable instructions.
5. Update both English and বাংলা versions together when a product feature, pricing or contract term changes.
6. Preserve evidence and approval records in appropriate controlled systems; keep secrets, client identification or private data out of this **public repository**.
7. For production website URLs, create tested 301 redirects, update internal links/sitemaps/canonicals/hreflang and inspect search impact after migration.
8. Never force push or rewrite published Git history to hide prior decisions without owner authorization.

## Version numbering
- **v1.0 draft:** first content specification.
- **v1.x:** editorial enhancements and verified correction without semantic reorganization.
- **v2.0:** new product release, feature matrix or architecture requiring broad content updates.

## Change request template
- Request ID/date:
- Files/categories:
- Why change:
- Previous version/commit:
- Proposed replacement:
- Product evidence:
- Impacted EN + BN / URL / schema / pricing pages:
- Approver:
- Merge/deployment status:
- Rollback plan:
