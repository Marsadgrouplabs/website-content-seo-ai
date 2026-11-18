# Default Output Package and Publish QA

Use this order unless the user asks for a smaller deliverable. Keep publishable copy visually separate from research and editor notes.

## Contents

1. Full output package
2. Publishable-copy rules
3. Hard gates
4. Detailed QA
5. Measurement
6. Compact mode

## 1. Full output package

### A. Page decision and assumptions

- Website/page type/current or proposed URL/date.
- `CREATE`, `UPDATE`, `MERGE`, or `HOLD` with rationale.
- Target audience, market, language/dialect, awareness stage, and conversion.
- Recommended content depth and evidence-based reason.
- Assumptions and research/access limitations.

### B. Facts and evidence ledger

| Claim/asset | Permitted wording | Source/date | Status | Scope | Limitation/HOLD |
|---|---|---|---|---|---|

Status options: `owner confirmed`, `independently verified`, `first-party system`, `publicly claimed only`, `conflicting`, `unknown`, `expired`.

### C. Research brief

- Existing URL/intent map and overlap.
- Keyword and intent clusters with sources/locale/date.
- Google Trends findings and limitations.
- Customer questions and community language from Reddit, Quora, reviews, forums, support/sales, or other relevant sources.
- SERP features and full page-one inventory for approved queries.
- Competitor comparison: table stakes, strengths, gaps, proof, CTA, and opportunities.
- AI-search test findings or `NOT TESTED`, with prompt-set limits.

### D. Content strategy and section map

| Section | Visitor decision/question | Fact/proof needed | Keyword/intent role | CTA/link |
|---|---|---|---|---|

Include page purpose, primary topic, supporting clusters, information gain, differentiation, and what belongs on another page.

### E. Publishable page copy

Deliver clean visitor-facing copy with:

- SEO title;
- meta description;
- proposed/existing slug and canonical decision;
- H1;
- complete section copy and headings;
- primary and secondary CTA text;
- form microcopy and response expectation when applicable;
- labels, captions, tables, product/card copy, or FAQ answers needed by the page.

Do not insert citations, research caveats, placeholders, schema notes, or editor instructions into visitor copy unless the user specifically wants sourced editorial content.

### F. SEO and entity package

- title/H1/meta rationale and alternatives only when materially useful;
- incoming/outgoing internal-link map with suggested anchors;
- structured-data recommendation, entity relationship, required facts, and warnings;
- Open Graph/social-share title, description, and image guidance when the page is likely to be shared or used in campaigns;
- image/video suggestions, provenance, filenames where useful, captions, and alt text;
- navigation/breadcrumb/category/location implications;
- indexability, canonical, pagination/facet/hreflang notes as applicable.

Provide JSON-LD only when the user requests it or implementation is in scope and every field is verified. Otherwise provide the schema plan and missing-data list.

### G. Conversion package

- primary conversion and qualified outcome;
- CTA hierarchy and placement;
- form fields with reason for each required field;
- trust/proof placement;
- objection and risk-reversal coverage;
- post-click/post-submit expectation;
- experiment hypotheses, not guaranteed uplifts.

### H. QA and release decision

- factual/claims QA;
- SEO/AI-search QA;
- conversion/UX/accessibility QA;
- technical/entity/schema QA;
- duplication/spam/policy QA;
- `PASS`, `PASS WITH OPEN ITEMS`, `MERGE`, or `HOLD`.

Name each unresolved item, owner, and exact resolution. Never convert a blocker into plausible-sounding copy.

### I. Measurement plan

- current baseline if actual data exists;
- events and qualified-conversion definition;
- page/query/country/device segments;
- brand/non-brand, organic/local/shopping/AI referral or reporting distinctions;
- launch/change log and review windows suitable to traffic volume;
- what outcome would trigger the next revision.

## 2. Publishable-copy rules

- Write for the target reader and market, not for the research report.
- Use an answer-first structure when the user needs a direct answer; use persuasion only after the offer is clear.
- Keep paragraphs and sentences scannable without chopping every thought into artificial “AI chunks.”
- Use headings for user navigation, not keyword decoration.
- Integrate terms naturally and cover concepts; never chase density.
- Put decisive information near the point of uncertainty: price, fit, scope, availability, returns, location, risk, and next step.
- Tie benefits to mechanisms, features, deliverables, evidence, or limitations.
- Add third-party sources, statistics, or expert quotations only when they materially support a visitor decision. Prefer current primary sources, verify the method/date/context, preserve quotation rights and attribution, and never insert evidence merely to chase an AI-citation tactic.
- Use real specificity. Replace vague `best`, `leading`, `innovative`, `premium`, and `world-class` with proof—or remove them.
- Do not state a competitor's weakness unless verified, fair, current, and necessary.
- Preserve legal, product, medical, technical, and brand terminology; explain it in plain language where needed.

## 3. Hard gates

Issue `HOLD` when any applicable item remains:

- Core product/service/location/price/availability claim is unconfirmed or contradictory.
- Page would duplicate an existing intent owner or create doorway/scaled-content risk.
- Page's only differentiation is keywords, city names, or paraphrased competitor copy.
- Client/customer/project/review/quote/result/media lacks permission or truthful attribution.
- Regulated or safety advice lacks a current primary source and required expert review.
- CTA, phone, checkout, form, or booking path is broken or misleading.
- Product feed, visible page, price/availability, and schema materially conflict.
- Location page implies a false branch/address/map presence.
- Critical robots/noindex/canonical/HTTP/security issue blocks intended publication.
- Claims rely on fabricated statistics, credentials, scarcity, timelines, guarantees, or AI output.

Recommend `MERGE` when the page cannot add standalone decision value or a current page already owns the intent.

## 4. Detailed QA

### Intent and usefulness

- [ ] Page satisfies the intended task without forcing the visitor through a thin intermediary.
- [ ] Page type matches the observed search intent and conversion stage.
- [ ] Essential questions and objections are answered in priority order.
- [ ] The page adds verified decision value beyond competitors and sibling pages.
- [ ] Content depth is justified; no section exists only to increase length.

### Facts, proof, and safety

- [ ] Every checkable claim appears in the claim register.
- [ ] Price, availability, hours, scope, qualifications, specifications, integrations, policies, and results are current.
- [ ] Quotes, logos, reviews, ratings, projects, and images are real, permissioned, and accurately attributed.
- [ ] No generated first-hand experience, fake expert, fabricated case study, or stock/AI media misrepresentation.
- [ ] High-stakes statements use primary sources and appropriate review.
- [ ] Conditions, exclusions, and uncertainty are clear where material.

### Search and AI visibility

- [ ] Primary topic and supporting concepts appear naturally in prominent and useful locations.
- [ ] Title, H1, intro, sections, and internal anchors describe the page consistently.
- [ ] Metadata, alt text, schema, and feeds were fact-checked, not only body copy.
- [ ] `nosnippet`, `max-snippet`, `max-image-preview`, `data-nosnippet`, and X-Robots-Tag do not unintentionally restrict the intended Search/AI presentation.
- [ ] No long-tail doorway expansion, FAQ stuffing, copied competitor phrasing, or scaled low-value pattern.
- [ ] AI-search observations are dated, reproducible enough to interpret, and not sold as guarantees.
- [ ] Standard SEO and crawlability take priority over unverified GEO hacks.
- [ ] No hidden prompt instructions, model-targeted manipulation, white-on-white text, HTML-comment injection, or unreviewed UGC instructions are present.

### Conversion and UX

- [ ] Primary CTA is clear and appropriate to awareness/commitment.
- [ ] Secondary CTA has a distinct purpose and does not compete unnecessarily.
- [ ] Proof sits near the claim or decision it supports.
- [ ] Forms request only needed information, with labels, privacy/consent, errors, success state, and response expectation.
- [ ] Price/commitment/returns/shipping/scope/location/availability information is not deliberately hidden.
- [ ] Page is readable and actionable on mobile and by keyboard/screen-reader users.
- [ ] No fake urgency, dark pattern, misleading button, preselected consent, or obstructive popup.

### Technical, schema, and entity

- [ ] HTTP, robots, noindex, canonical, sitemap, and redirect status support the page goal.
- [ ] Crawlable internal links connect the page into a useful hierarchy.
- [ ] Structured data describes visible verified content and does not conflict with plugins/feed/sitewide entity.
- [ ] Visible dates and `datePublished`/`dateModified` agree where dates are used; modified dates reflect material updates rather than automatic refreshes.
- [ ] Google-supported rich-result requirements are distinguished from generic schema.org vocabulary.
- [ ] Organization/location/product/contact facts are consistent sitewide and across external systems.
- [ ] Facets, parameters, pagination, variants, currencies, and localized URLs have intentional index/canonical handling.
- [ ] Media is authorized, compressed, correctly dimensioned, accessible, and accurately captioned.

### Editorial and localization

- [ ] Language, dialect, tone, currency, units, dates, phone/address format, and terminology fit the market.
- [ ] Copy is original and not a sentence-by-sentence rewrite of a competitor.
- [ ] No generic AI filler, repetitive conclusion, forced FAQ, or inflated adjective pattern.
- [ ] Editor notes, sources, placeholders, and internal statuses are absent from visitor copy.
- [ ] Grammar, punctuation, link destinations, names, and numerical consistency are checked.

## 5. Measurement

Measure the commercial chain, not visibility alone:

1. eligibility/indexing and accurate feed/entity data;
2. impressions/mentions/citations;
3. visits or referral traffic;
4. meaningful page action;
5. contact, add-to-cart, checkout, signup, or booking;
6. qualified lead/sale/retention outcome.

Clicks on a phone link are not confirmed calls; form starts are not successful submissions; leads are not sales. Define events accordingly and protect personal data.

Use GSC/AI performance reports, analytics, Merchant Center, GBP, CRM, call tracking, and AI referral/controlled prompt tests where available. Compare appropriate windows and account for seasonality, campaigns, product availability, brand demand, local events, and algorithm updates. Do not attribute every change to page copy.

Review windows such as 28/56/90 days may be useful for ordinary sites, but low-traffic or seasonal pages need longer or qualitative evidence. Record the exact change and launch date.

## 6. Compact mode

When the user requests only content, return:

1. short page decision and critical assumptions;
2. SEO title, meta description, H1, and slug/canonical note;
3. clean publishable copy;
4. concise internal-link/media/schema suggestions;
5. only the factual or release holds that materially affect publication.

Do not remove research rigor; reduce report length, not evidence quality.
