# Schema, Technical SEO, Entity, and Implementation Rules

Use current official documentation at implementation time. Schema.org vocabulary, Google-supported rich-result types, Merchant Center requirements, and AI-search eligibility are not interchangeable.

## Contents

1. Core technical checks
2. Titles, snippets, headings, and URLs
3. Internal links and architecture
4. Page-type schema map
5. Ecommerce implementation
6. Local and entity implementation
7. AI crawler and visibility checks
8. Media, accessibility, and page experience
9. Internationalization

## 1. Core technical checks

Before recommending publication, inspect when access permits:

- intended HTTP status and final redirect target;
- robots.txt access, robots meta/X-Robots-Tag, and Search/AI controls;
- snippet and preview controls, including `nosnippet`, `max-snippet`, `max-image-preview`, and material `data-nosnippet` use, when the page is intended for Search or generative Search visibility;
- canonical target and duplicate variants;
- crawlable HTML content and `<a href>` links;
- XML sitemap and navigational discoverability;
- mobile rendering, forms, buttons, error/success states, and JavaScript dependencies;
- structured-data duplication/conflict across theme, plugins, feed, and custom code;
- visible dates and `datePublished`/`dateModified` consistency when dates are present or freshness matters; never auto-refresh a modified date without a material page update;
- hidden text, HTML comments, untrusted embeds, or UGC that contains instructions aimed at manipulating AI systems or overriding extraction behavior;
- security/hacked spam signs that can invalidate otherwise good content.

Do not call a writing problem “technical SEO” or a crawl issue “content quality.” Report them separately.

## 2. Titles, snippets, headings, and URLs

- Create a descriptive, concise title that reflects the page's primary purpose and entity. Avoid repetitive boilerplate and keyword stuffing.
- Align title, visible H1, prominent page text, and internal anchors without making them mechanically identical.
- Write a useful meta description as a possible snippet, not a guaranteed display or ranking factor. Include the decision value and next step where natural.
- Use one clear page-level H1 in ordinary implementations, followed by a logical heading hierarchy. Do not choose headings solely to insert queries.
- Recommend short, readable URLs using hyphens for word separation for new URLs. Do not rename working URLs merely to match a preferred style.
- Preserve established URLs unless a documented migration benefit outweighs risk. When changing, use the correct redirect, update canonicals, links, sitemap, hreflang, feeds, and tracking.

There is no fixed Google ranking rule for a 60-character title, 160-character description, or minimum page word count. Preview truncation varies.

## 3. Internal links and architecture

Map both directions:

- incoming links from navigation, hubs, categories, related services/products, case studies, and guides;
- outgoing links to the next decision step, detailed policies, evidence, related offers, and parent/child pages.

Use crawlable links and concise, descriptive anchors. Avoid keyword link farms, circular city/service blocks, sitewide links to every landing page, and links that exist only for PageRank theories.

For ecommerce, expose a crawlable path from menus → categories → subcategories → products. A search box alone is not discoverability. Handle pagination and facets so important products are reachable without creating uncontrolled indexable combinations.

## 4. Page-type schema map

Always represent visible, verified content. Validate syntax with Schema Markup Validator and Google eligibility with Rich Results Test where the type is supported. Passing validation never guarantees display.

| Page type | Reasonable vocabulary | Google/implementation caution |
|---|---|---|
| Homepage | `WebSite`, one canonical `Organization` or eligible `LocalBusiness` entity | Google recommends Organization details on the homepage; do not create multiple conflicting entities. |
| About | `AboutPage` linked to the canonical organization | No special About-page rich result. Use factual visible details. |
| Contact | `ContactPage`; organization `contactPoint` where applicable | Keep phone/email/address consistent and visible; do not invent departments or response hours. |
| Service | `Service`, `WebPage`, `BreadcrumbList`, real provider entity | `Service` is useful vocabulary but not a promised Google service rich result. |
| Ecommerce product | `Product` + eligible `Offer`/variants/shipping/returns fields | Merchant listings apply to purchasable single products or legitimate variants, not category lists. Keep feed, visible page, and markup synchronized. |
| Lead-gen product | `Product`; eligible specialist type such as `SoftwareApplication` only when current requirements are met | Do not force a rich-result type or represent a demo/quote page as direct purchase. |
| Category/collection | `CollectionPage`, optional honest `ItemList`, `BreadcrumbList` | Do not attach single-product merchant listing markup to the category. |
| Landing | `WebPage` and an existing canonical entity | There is no special “LandingPage” ranking schema. Decide index/canonical by campaign role. |
| Pricing | `WebPage`; semantically accurate `Offer`/`OfferCatalog` only if visible and maintained | No special pricing rich result; do not encode hidden or expired prices. |
| Physical location | Most specific eligible `LocalBusiness`, true address/hours/phone, `BreadcrumbList` | One real location per entity/page as appropriate; follow current GBP and Google structured-data rules. |
| Service area | `WebPage`/`Service`; canonical provider may use truthful `areaServed` | Do not create a fake city `LocalBusiness`, address, map pin, or branch. |
| FAQ | `FAQPage` only for visible, genuine FAQ content if another consumer needs it | Google FAQ rich results ended 7 May 2026; do not promise visibility. |
| Case study | `Article`, `CreativeWork`, or a more accurate subtype; canonical organization | No special case-study rich result. Do not use `Review` to manufacture self-serving ratings. |

Do not add schema fields merely because they exist. Omit unknown properties. Never put a claim only in structured data to avoid displaying it to users.

## 5. Ecommerce implementation

- Keep price, sale price, currency, availability, condition, variants, shipping, returns, and identifiers consistent across visible content, structured data, Merchant Center feed, checkout, and country/currency URLs.
- Use a distinct URL per currency when current Google merchant guidance requires it; preserve legitimate variant/canonical logic.
- Put Product markup in initial HTML where feasible for fast-changing price/availability reliability.
- Use authentic product images and accurate alt/context. If AI-generated product data or imagery is used, follow current Merchant Center labeling and IPTC metadata policies.
- Do not publish unavailable variants as in stock, fake ratings, reviews copied without rights, or delivery promises unsupported by fulfillment.
- For category pages, make all indexable products discoverable through links, pagination, sitemap, or feed as appropriate.

## 6. Local and entity implementation

Maintain one coherent entity across homepage, About, Contact, footer, schema, GBP, citations, directories, and location pages:

- business/trading/legal names as applicable;
- real address or clearly stated service-area model;
- phone, email, hours, and appointment rules;
- actual locations, departments, and service areas;
- logos, profiles, identifiers, and verified credentials.

A service-area page cannot manufacture proximity. Local results depend on relevance, distance, and prominence, and textual optimization does not erase distance. Do not create virtual-office listings or a GBP for every served city.

Use `Organization` on the homepage to help disambiguate the entity. Add `sameAs`, identifiers, address, telephone, email, logo, return/shipping policy, or contact points only when true, public, and relevant.

## 7. AI crawler and visibility checks

- Google generative search depends on normal Search eligibility and current Search generative AI controls. Follow official Search Console documentation.
- Treat crawler purposes separately: automatic search/indexing, model training, and user-triggered retrieval are different controls. Do not copy one bot rule to every crawler.
- For Google, `Googlebot` and snippet/indexing controls govern Google Search and its generative Search features; `Google-Extended` is a separate control for specified Gemini/Vertex training or grounding uses and is not a Google Search ranking control.
- OAI-SearchBot controls ChatGPT search discovery independently from GPTBot training. Check robots.txt, WAF/CDN, response codes, and OpenAI's published IP guidance; allowing access does not guarantee placement.
- Treat ChatGPT-User or other user-triggered fetchers differently from automatic search crawlers according to current official docs.
- Anthropic currently documents `Claude-SearchBot` for search, `ClaudeBot` for potential model-training collection, and `Claude-User` for user-triggered retrieval. Recheck the official Claude Help Center before changing rules.
- Check the relevant current documentation for Perplexity, Bing/Copilot, and other requested systems rather than assuming one crawler policy covers all.
- Do not weaken WAF/security globally or trust a user-agent string alone. Verify provider documentation and logs.
- `llms.txt`, tiny content chunks, special AI schema, or fake mentions are not Google ranking requirements. Create such files only for a defined consumer/use case and explain the limit.
- Training controls and search/citation controls are separate. Google announced a shared AI-training preference proposal on 30 October 2026 with intended support in 2027; do not represent the proposal as a current search-ranking feature.
- If a third-party GEO audit reports a score or auto-fix list, record its tool and rubric version and treat it as a diagnostic checklist only. Verify every crawler, schema, metadata, and content recommendation against current official documentation and visible facts before applying it; never call the score a Google, ChatGPT, Perplexity, or Claude score.

Official controls to recheck:

- Google robots/snippet controls: https://developers.google.com/search/docs/crawling-indexing/robots-meta-tag
- OpenAI crawlers: https://developers.openai.com/api/docs/bots
- Anthropic crawlers: https://support.claude.com/en/articles/8896518-does-anthropic-crawl-data-from-the-web-and-how-can-site-owners-block-the-crawler

## 8. Media, accessibility, and page experience

- Use original/authorized media that helps the decision. Never depict AI/stock media as a real team, facility, product, project, or result.
- Write alt text that describes the image's purpose and visible content; use empty alt for decorative imagery where appropriate. Do not stuff locations or keywords.
- Supply captions when provenance, place, person, result, or product variant matters.
- Compress and size media, avoid layout shifts, and lazy-load non-critical assets. Do not lazy-load the main above-the-fold image in a way that harms rendering.
- Ensure readable contrast, keyboard focus, accessible labels, logical reading order, descriptive errors, and touch-friendly controls.
- Treat Core Web Vitals and lab scores as page-experience diagnostics, not guaranteed ranking outcomes.

## 9. Internationalization

- Research each target market's language and search behavior; do not translate keywords literally without checking usage.
- Localize currency, units, dates, address/phone format, legal terms, delivery/service availability, dialect, and cultural expectations.
- Use correct language/region URLs and reciprocal hreflang where multiple localized versions exist; keep canonical logic compatible.
- Do not mass-translate pages primarily for search without local review and independent usefulness.
- Preserve brand/product names and regulated terminology accurately. Require a qualified reviewer for high-stakes localization.
