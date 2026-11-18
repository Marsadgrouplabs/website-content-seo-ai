# SEO, AI Search, UX, and Conversion Research Baseline

**Research cutoff:** 31 October 2026. Recheck live official sources whenever current policy, eligibility, crawler behavior, or a recently changed feature matters.

Use the labels `OFFICIAL`, `EMPIRICAL`, `EXPERIMENT`, `OBSERVATIONAL`, and `EDITORIAL`. A case study is evidence about one treatment and context, not a universal forecast.

## Contents

1. Current Google updates
2. Content and AI-assisted writing
3. AI-search discovery and citations
4. Keyword, Trends, and measurement
5. Page-type UX and conversion evidence
6. What not to claim
7. Source register

## 1. Current Google updates

### Ranking status [OFFICIAL]

Google's Search Status Dashboard lists these latest completed ranking incidents as of the cutoff:

- September 2026 spam update: 24 September–8 October 2026, global and all languages.
- August 2026 spam update: 18–21 August 2026.
- June 2026 spam update: 24–26 June 2026.
- May 2026 core update: 21 May–2 June 2026.

The dashboard does not disclose a page-level detector or prove why a specific URL moved. Do not attribute losses or gains to AI content, page length, schema, or another single element without site-specific evidence and change logs.

Source: https://status.search.google.com/summary

### October 2026 documentation changes [OFFICIAL]

- **30 October:** Google announced plans to support a shared robots.txt AI-training preference based on the IETF AIPREF work, targeting 2027 support. It is a future training-control proposal, not a current ranking or citation signal. Existing provider-specific controls remain distinct.
- **26 October:** updated user-generated-spam prevention guidance, including index blocking for link-shared content and Search Console monitoring.
- **23 October:** clarified hyphens as word separators in crawlable URL guidance. This is not a reason to bulk-rename working URLs.
- **21 October:** updated documentation on controlling what is shared with Search, covering robots meta, `data-nosnippet`, `X-Robots-Tag`, and Search generative AI controls.
- **1 October:** updated generative-AI content guidance to stress value, manual fact-checking, low-effort/low-originality risks, and review of metadata, alt text, and structured data.

Sources:

- https://developers.google.com/search/updates
- https://developers.google.com/search/blog/2026/10/ai-training-control
- https://developers.google.com/search/docs/monitor-debug/prevent-abuse
- https://developers.google.com/search/docs/fundamentals/using-gen-ai-content

### Spam and people-first rules [OFFICIAL]

- Scaled content abuse concerns many pages produced mainly to manipulate rankings with little user value, regardless of whether AI or humans created them.
- Doorway abuse includes substantially similar pages for cities/regions or queries that act as less-useful intermediaries.
- Helpful content guidance emphasizes original information, substantial value, clear `who/how/why`, and a visitor-first purpose—not a fixed length, density, or AI percentage.
- Site reputation abuse is a different policy concerning third-party content exploiting a host's established signals; do not misuse it as a label for ordinary first-party service pages.

Sources:

- https://developers.google.com/search/docs/essentials/spam-policies
- https://developers.google.com/search/docs/fundamentals/creating-helpful-content
- https://developers.google.com/search/blog/2026/08/update-site-reputation-policy

## 2. Content and AI-assisted writing

### Google guidance [OFFICIAL]

Google says generative AI can assist research and structure, but low-value scaled generation may violate spam policy. Manual review must cover body copy and metadata, titles, descriptions, alt text, and structured data. Disclosure/context may help readers when automation materially affects content.

For Google generative search, foundational SEO, indexability, clear technical structure, useful non-commodity content, and relevant images/video remain core. Google explicitly says it does not require `llms.txt`, tiny “chunks,” special AI markup, exact long-tail variants, or inauthentic mentions.

Sources:

- https://developers.google.com/search/docs/fundamentals/using-gen-ai-content
- https://developers.google.com/search/docs/fundamentals/ai-optimization-guide

### AI-content studies [OBSERVATIONAL]

- Ahrefs' 27 July 2026 study of about 331,000 pages found high estimated AI-content pages can rank, while its sampled indexation rate was lower in the very-high-AI group than the low-AI group. Detector uncertainty, domain/content quality, and selection effects prevent a causal “AI penalty” claim.
- Semrush's April 2026 analysis of 42,000 articles/20,000 queries reported different ranking distributions by classified authorship and a survey of SEO opinions. It was not a randomized test and should not become an AI-percentage threshold.
- Ahrefs' 2025 prevalence study estimated much new English web content contained some AI text; prevalence does not prove quality or ranking effect.

Application: use AI for research, outlining, comparison, and drafting grounded in verified first-party information. Measure usefulness, accuracy, distinct value, and outcomes—not detector scores.

Sources:

- https://ahrefs.com/blog/google-doesnt-punish-ai-content/
- https://www.semrush.com/blog/does-ai-content-rank-in-search-data-study/
- https://ahrefs.com/blog/what-percentage-of-new-content-is-ai-generated/

## 3. AI-search discovery and citations

### Google generative features [OFFICIAL]

Eligibility depends on normal Search indexing/snippet eligibility and current Search generative AI controls. Google says generative features use its retrieval/ranking systems and can surface products and local businesses through standard web, Merchant Center, and GBP data. Search Console added dedicated generative AI performance reporting in June 2026.

Sources:

- https://developers.google.com/search/docs/fundamentals/ai-optimization-guide
- https://support.google.com/webmasters/answer/16984139
- https://developers.google.com/search/blog/2026/06/gen-ai-performance-reports

### ChatGPT discovery [OFFICIAL]

OpenAI documents OAI-SearchBot for ChatGPT search and GPTBot separately for model training. A publisher can allow search discovery while disallowing training. Check robots.txt, the CDN/WAF, response codes, and published IP ranges. Allowing access makes inclusion possible; placement is not guaranteed. ChatGPT-User is user-triggered and is not the automatic search crawler.

Sources:

- https://developers.openai.com/api/docs/bots
- https://help.openai.com/en/articles/9237897-chatgpt-search

### Claude discovery [OFFICIAL]

Anthropic's crawler documentation, updated 7 April 2026, separates three purposes: `Claude-SearchBot` for search-quality indexing, `ClaudeBot` for public-web collection that may contribute to model training, and `Claude-User` for user-triggered retrieval. Site owners can control them separately through robots.txt. Recheck the official page before implementation because bot behavior and identifiers can change.

Source: https://support.claude.com/en/articles/8896518-does-anthropic-crawl-data-from-the-web-and-how-can-site-owners-block-the-crawler

### Perplexity discovery [OFFICIAL]

Use the current Perplexity crawler documentation for PerplexityBot and user-triggered fetch behavior. Do not assume OpenAI or Google crawler rules apply to Perplexity, and do not disable bot protection globally.

Source: https://docs.perplexity.ai/docs/resources/perplexity-crawlers

### Citation research [EMPIRICAL/OBSERVATIONAL]

- Chen and Koudas' 10 October 2026 preprint analyzed two 90-day commercial-query collections totaling 158,099 answers and 468,037 citations. Within websites, semantic match between page titles/paragraphs and questions related to citations, but retrieval behavior explained much more variation than measured page features in their ChatGPT replay. FAQ blocks, schema, summary boxes, and speed did not establish a universal within-site citation advantage. This is a large but still domain/model/time-specific preprint.
- `Answer Bubbles` (Findings of EMNLP 2026) compared 11,000 queries across generative and traditional systems and found material source-selection and citation-fidelity differences. It demonstrates that AI surfaces are not interchangeable and that citation bias/variability must be measured, not assumed.
- A 2026 study comparing Google Search, Gemini, and AI Overviews on 11,500 queries reported low overlap and instability across systems/query edits. Treat the exact percentages as study-specific, not an expected rate for a client.
- Ahrefs' October 2026 analysis of logged-out ChatGPT answers observed query fan-out patterns, including brand/site and official-fact queries. It is a snapshot of one setup, not proof that creating pages for every fan-out query will improve visibility.

Application:

- Test representative prompts on each requested platform and repeat a subset.
- Make authoritative business/product facts, pricing/availability, scope, and original evidence easy to retrieve on the correct page.
- Match real questions semantically in titles and paragraphs without duplicating a page for every phrasing.
- Measure mention, citation, recommendation, accuracy, referral, and conversion separately.

Sources:

- https://arxiv.org/abs/2610.15033
- https://aclanthology.org/2026.findings-emnlp.8/
- https://arxiv.org/abs/2604.27790
- https://ahrefs.com/blog/query-fan-out-chatgpt/

## 4. Keyword, Trends, and measurement

### Keyword Planner [OFFICIAL]

Average monthly searches reflect close variants and selected date/location/Search Network settings. “Competition” is advertiser competition. Record settings and do not label it organic difficulty.

Sources:

- https://support.google.com/google-ads/answer/3022575
- https://support.google.com/google-ads/answer/7337243

### Google Trends [OFFICIAL]

Trends uses a sampled, normalized index scaled 0–100 for the chosen time/location context. Equal index values in different regions do not imply equal absolute volume; zero may mean insufficient data. Use terms/topics, geography, period, category, and search type carefully, and compare within the same chart.

Sources:

- https://support.google.com/trends/answer/4365533
- https://support.google.com/trends/answer/4355000

### Search Console [OFFICIAL]

GSC is first-party Search performance, but its tables and dimensions can be aggregated or truncated and usually group data by canonical URL. Segment page/query/country/device/date and distinguish web, image, Discover, generative AI, and other reports. Do not equate GSC with analytics sessions or third-party traffic estimates.

Sources:

- https://support.google.com/webmasters/answer/7576553
- https://support.google.com/webmasters/answer/17011259
- https://support.google.com/webmasters/answer/16984139

## 5. Page-type UX and conversion evidence

### About and Contact [EMPIRICAL UX]

Nielsen Norman Group's corporate-site research tested 100 sites and reviewed 65 more for About guidance. It found users need a plain explanation of what an organization does, concise summaries, authentic imagery, explicit navigation labels, and easy contact information. Its Contact study with 20 business professionals across 40 corporate sites found users expect a dedicated page with complete, direct contact options, availability, and response expectations—not only a form.

These studies are older than the cutoff and focused heavily on corporate/B2B use; the underlying task expectations are stable, but each market's channels/privacy rules must be rechecked.

Sources:

- https://www.nngroup.com/articles/about-us-information-on-websites/
- https://www.nngroup.com/articles/contact-us-pages/

### Ecommerce product and category pages [EMPIRICAL UX]

Baymard's Product Page UX benchmark, updated 18 March 2026, summarizes more than 30,000 manually rated product-page performance scores across 155+ leading US/European sites. It highlights decision friction around variant visibility, total cost, return information, reviews, imagery, and mobile UX. The benchmark shows widespread problems, not a guaranteed uplift from copying any one pattern.

Baymard's 2025–2026 product-list and homepage/category work emphasizes meaningful filtering, product-card decision information, visible category pathways, and mobile usability. Match recommendations to the store's catalog and user research.

Sources:

- https://baymard.com/research-articles/current-state-ecommerce-product-page-ux
- https://baymard.com/research-articles/current-state-product-list-and-filtering
- https://baymard.com/research-articles/ecommerce-navigation-best-practice

### Ecommerce Search implementation [OFFICIAL]

Google recommends crawlable navigation from menus to categories/subcategories/products, and warns that Googlebot generally does not submit onsite search forms. Product rich-result/merchant markup targets a single product or legitimate variants, not category lists. Keep visible product data, structured data, and Merchant Center feeds consistent.

Sources:

- https://developers.google.com/search/docs/specialty/ecommerce/help-google-understand-your-ecommerce-site-structure
- https://developers.google.com/search/docs/appearance/structured-data/merchant-listing
- https://developers.google.com/search/docs/specialty/ecommerce/share-your-product-data-with-google
- https://developers.google.com/search/docs/specialty/ecommerce/pagination-and-incremental-page-loading

### Landing pages [OBSERVATIONAL BENCHMARK]

Unbounce's current Conversion Benchmark methodology uses data from 23 July 2023–23 July 2024: 464 million visitors, 57 million conversions, and 41,000 landing pages, excluding thin samples. It reports industry-specific differences in conversion, readability, and copy length. The dataset is large but platform-specific, historical, and correlational; never turn a reported word-count band, reading level, or median into a universal target.

Application: use industry context to form hypotheses, then test message match, clarity, offer, proof, friction, device experience, and form commitment on the actual traffic.

Sources:

- https://unbounce.com/conversion-benchmark-report/methodology/
- https://unbounce.com/conversion-benchmark-report/

### Pricing, case studies, and internal links [OBSERVATIONAL/EXPERIMENT]

- HockeyStack Labs reported page-level patterns from 31 million unique visitors across 80 B2B SaaS companies for pricing, demo, and case-study pages. The sample is vendor/platform specific and cannot prove transparent pricing or a page type causes a particular conversion rate.
- SearchPilot's 30 September 2026 ecommerce experiment reported a positive organic effect from targeted internal links to product-listing pages; its separate March 2026 destination-link test was inconclusive. This supports testing relevant architecture, not adding a fixed number of links or importing the uplift.
- SearchPilot's 6 November 2025 ecommerce test adding AI-written product highlights with disclosure reported a positive measured result. The treatment added useful content and AI authorship together, so it does not isolate “AI” as the cause or transfer directly to other page types.

Sources:

- https://www.hockeystack.com/lab-blog-posts/state-of-pricing-demo-case-study-pages
- https://www.searchpilot.com/resources/case-studies/how-we-increased-organic-pdp-traffic-by-18-percent
- https://www.searchpilot.com/resources/case-studies/can-popular-destinations-links-improve-seo
- https://www.searchpilot.com/resources/case-studies/what-happens-to-traffic-when-ai-content-is-added-with-a-disclaimer

### FAQ change [OFFICIAL]

Google stopped displaying FAQ rich results on 7 May 2026 and removed associated reporting/testing support. FAQs can still help users, and `FAQPage` remains schema.org vocabulary, but do not promise a Google rich result or AI citation.

Sources:

- https://support.google.com/webmasters/answer/6211453
- https://developers.google.com/search/updates

## 6. What not to claim

Do not claim:

1. Google penalizes a fixed percentage of AI text or rewards human text as a direct signal.
2. A fixed word count, keyword density, reading grade, title length, schema type, or number of links ranks a page.
3. Ranking competitors prove their copy/layout caused the ranking.
4. `llms.txt`, FAQ schema, “AI chunks,” or a special GEO markup is required for Google AI visibility.
5. Allowing an AI crawler guarantees citation or recommendation.
6. One AI answer represents stable share of voice.
7. A forum question proves search volume, truth, or common prevalence.
8. A location statement makes city-swap pages safe from doorway/scaled-content risk.
9. A case-study conversion or traffic uplift transfers to another site, industry, or page.
10. Search Console, analytics, Merchant Center, GBP, third-party SEO tools, and AI prompt tests measure the same thing.
11. A third-party GEO score is an official Google, ChatGPT, Perplexity, or Claude score, or that its auto-fixes are safe to apply without page-level review.

## 7. Core source register

- Google Search docs updates: https://developers.google.com/search/updates
- Google Search status: https://status.search.google.com/summary
- Google AI-assisted content: https://developers.google.com/search/docs/fundamentals/using-gen-ai-content
- Google generative AI optimization: https://developers.google.com/search/docs/fundamentals/ai-optimization-guide
- Google helpful content: https://developers.google.com/search/docs/fundamentals/creating-helpful-content
- Google spam policies: https://developers.google.com/search/docs/essentials/spam-policies
- Google titles/snippets/links: https://developers.google.com/search/docs/appearance/title-link ; https://developers.google.com/search/docs/appearance/snippet ; https://developers.google.com/search/docs/crawling-indexing/links-crawlable
- Google Organization/LocalBusiness: https://developers.google.com/search/docs/appearance/structured-data/organization ; https://developers.google.com/search/docs/appearance/structured-data/local-business
- Google ecommerce/Product: https://developers.google.com/search/docs/specialty/ecommerce ; https://developers.google.com/search/docs/appearance/structured-data/product
- OpenAI crawlers: https://developers.openai.com/api/docs/bots
- Anthropic crawlers: https://support.claude.com/en/articles/8896518-does-anthropic-crawl-data-from-the-web-and-how-can-site-owners-block-the-crawler
- Perplexity crawlers: https://docs.perplexity.ai/docs/resources/perplexity-crawlers
- Google Trends data: https://support.google.com/trends/answer/4365533
- Google Search Console performance: https://support.google.com/webmasters/answer/7576553
