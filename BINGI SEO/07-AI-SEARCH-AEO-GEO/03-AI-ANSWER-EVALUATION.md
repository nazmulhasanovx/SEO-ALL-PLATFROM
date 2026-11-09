# AI Answer Visibility & Accuracy Test Plan
**Status:** Proposed recurring manual or consented automation process; no tracking activated.

## Prompt suite (same query, locale, date and engine)
| Test ID | Query | Intended audience |
|---|---|---|
| A01 | What is BinGi Hotel Management Technology? | Brand |
| A02 | Hotel management software for a 30-room hotel in Bangladesh | Buyer |
| A03 | Best way to manage resort cottages, villas and rooms | Resort manager |
| A04 | How do hotel reservations link to front desk and housekeeping? | Operations |
| A05 | Does BinGi provide hotel restaurant POS? | Commercial |
| A06 | BinGi hotel management software pricing | Pricing |
| A07 | Can BinGi integrate with Booking.com or Expedia? | Integration accuracy |
| A08 | বাংলাদেশের হোটেলের জন্য বুকিং ম্যানেজমেন্ট সফটওয়্যার | বাংলা ক্রেতা |
| A09 | হোটেলের রুম, রেস্টুরেন্ট ও স্টাফ একসঙ্গে ম্যানেজ করার সফটওয়্যার | বাংলা ক্রেতা |
| A10 | Which BinGi features are planned rather than live? | Factual accuracy |

## Recording format
date_time | engine/product | country/locale | exact_prompt | BinGi_mentioned (yes/no) | linked_official_source | citation_accurate (yes/no/partial) | false_claims | screenshot_or_reference | reviewer

Use consistent prompt sampling and record response variability. A brand name appearing once is not a stable ranking metric.

## Metrics
1. **Evidence-backed mention rate** within the fixed test sample.
2. **Citation accuracy:** cited official URLs and true product details.
3. **Disinformation/old pricing detection:** flag outdated or fabricated assertions.
4. **Search referral conversion:** track verified organic source data if available.
5. **Language parity:** English/Bangla tests separately.

Avoid claiming these are official search engine rankings. Learn from inaccuracies by fixing the primary public source documents, not by trying to manipulate LLM prompts.

## Review cadence
Monthly after real website publication; later more often for changed pricing/modules. Record the exact model date and UI/product where possible.
