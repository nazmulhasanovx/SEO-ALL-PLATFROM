# BinGi SEO Measurement Framework

## Primary outcome metrics
**Qualified organic demo requests** / trials / inbound sales leads with a traceable campaign or referral source. Define qualification with sales team: property, room capacity, location, decision-maker role, expected modules, timeline.

## Standard search KPIs
| KPI | Collection source | Caveat |
|---|---|---|
| Search clicks and impressions | Google Search Console | Separate domains, language paths and query classes |
| Indexed URL coverage and errors | Search Console URL Inspection, sitemaps | Indexing not guaranteed |
| Bing impressions and submitted URLs | Bing Webmaster Tools | IndexNow notification ≠ index inclusion |
| Organic landing sessions | Approved analytics platform | Consent, attribution and cookie settings |
| Organic demo-request completions | Form/backend confirmed + analytics event | Deduplicate leads and bot submissions |
| Non-branded query share | Search Console queries | Privacy/query aggregation may restrict access |
| English vs বাংলা results | URL segment and locale | Match actual page language |
| Search generative AI visibility | Available Search Console AI features and manual sample | Product/report availability can change |
| AI answer citation quality | Fixed prompt suite, timestamp, references | Anecdotal sample, not universal ranking |

## Events (proposal — not installed)
- `demo_request_start`
- `demo_request_submit`
- `trial_signup_complete`
- `contact_sales_submit`
- `module_walkthrough_click`
- `pricing_plan_inquiry_submit`

Track only necessary event metadata; **do not send guest details, employee identifiers, personal email, phone or payment information as analytics parameters**.

## Attribution
Record source/medium, landing page, content cluster, language, demo status and CRM outcome where appropriate and consent compliant. Remember direct or AI referral classification may differ across analytics tools.

## Baseline
Collect actual 28-day and 90-day baseline before setting growth percentages. No invented baseline metrics or numeric targets in reports.
