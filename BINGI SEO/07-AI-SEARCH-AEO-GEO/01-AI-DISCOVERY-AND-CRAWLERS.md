# Discoverability Across Search and AI Systems
**Date:** 2026-11-09 | **Status:** Proposed operational policy

## Retrieval is not training
- **Google Search / AI Overviews / AI Mode:** ordinary Google Search fundamentals remain relevant; eligible pages should be indexed and snippet-eligible. In 2026 Google also introduced a specific Search generative AI site inclusion control, which must be reviewed in Search Console.
- **Bing / Copilot:** maintain accessible search pages and verify indexing in Bing Webmaster Tools; IndexNow can notify Bing and other participating engines of URLs.
- **OpenAI / ChatGPT Search:** OpenAI states `OAI-SearchBot` is for search inclusion. `GPTBot` is separate and is related to potential foundation-model training. A website owner may permit search while opting out of training through its independent directives.
- **ChatGPT-User:** user-initiated browsing agent; not the automated search crawler.
- **Other providers:** check current official crawler docs before making new user-agent allow/deny promises.

## Engineering handoff
1. Fetch real robots.txt for **each host** and inspect CDN/firewall/logs.
2. Document the desired policy for Search vs training per user agent, based on product/legal preference.
3. Ensure intended public pages provide correct HTML, sitemap, internal links and a valid HTTP response.
4. Ensure private guest/staff/account endpoints use actual authentication and access control.
5. Test search crawler permission on real URLs and record date.
6. Monitor Google/Bing indexing and answer citation observations; these are separate from crawler allowance.

## 2026 Google generative AI control
Google publicly states the Search generative AI inclusion control was rolled out globally by **August 31, 2026**. A verified owner can examine it in Search Console under Settings. Record whether each verified property is included/opted out; don't assume status.

## Optional llms.txt
Treat as an auxiliary curated document index at most. Google says no special AI text files / markup are required for its generative AI search features. Never put private internal product instructions or customer data into public machine-readable files.

## Authoritative guidance
- https://developers.openai.com/api/docs/bots
- https://developers.google.com/search/docs/fundamentals/ai-optimization-guide
- https://developers.google.com/search/docs/appearance/ai-features
- https://support.google.com/webmasters/answer/16908024?hl=en
- https://www.bing.com/indexnow/getstarted
