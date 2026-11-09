# Deployment Configuration Template — No Secrets Here

```yaml
project: bingi-seo
mode: staging-only
enabled: false
sites:
  b2b:
    host: https://technology.bingi.com.bd
    cms_connection: MANAGED_SECRET_REFERENCE
  b2c:
    host: https://bingi.com.bd
    cms_connection: MANAGED_SECRET_REFERENCE
languages: [en, bn]
publishing:
  require_human_product_approval: true
  require_editor_approval: true
  require_final_release_approval: true
  verify_canonical_and_hreflang: true
  prevent_duplicate_slug: true
  production_publish_enabled: false
indexing:
  sitemap_refresh_after_publish: true
  indexnow_enabled: false
monitoring:
  record_publish_id: true
  collect_search_console_after_approval: false
```

This YAML is a **documentation example**, not a valid installed n8n workflow nor proof the CMS supports these options. Keep actual configuration in secured operations infrastructure.
