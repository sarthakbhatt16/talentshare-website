# talent-share website handoff

The 14-page website is a static marketing layer for app.talent-share.com. Program listings, provider profiles, prices, dates, enrollment, and account workflows remain in the app.

## Content approach

The homepage follows seeker need, the value of live learning, subject relevance, booking confidence, the program experience, and next steps. The provider page follows discovery and management problems, then explains how public profiles, program pages, and app tools address them. Supporting pages answer specific questions instead of repeating the entire feature list.

See `talentshare/CONTENT-STRATEGY.md` for the purpose and sequence of each page. Full page copy is in `TalentShare-Website-Content.md`. Titles, descriptions, and keyword targets are in `talentshare/seo-map.json`.

Brand spelling is talent-share. People who teach are providers, people who learn are seekers, and offerings are programs. Copy uses direct language and no long-dash punctuation.

## Evidence

Product facts come from the supplied TalentShare-Website-Feature-Brief.pdf. The existing www.talent-share.com site informed the original brand and the problems described in the marketing narrative. Public app pages were inspected, but dynamic information was excluded from the static marketing site.

The site contains no fabricated reviews, ratings, provider biographies, statistics, earnings promises, or live inventory. Photographs and interface examples are illustrative. AI assistance is described as optional writing help, with provider review before publishing. No payout-button, fee-percentage, tax, certification, or app-store availability claims are made.

## Launch

The review site remains private and noindex. The existing www.talent-share.com site has not been replaced.

For production, build with `SITE_ORIGIN=https://www.talent-share.com PRODUCTION=1`. Preserve existing legal/privacy content and the `/legal` route. Configure redirects from old marketing URLs when migrating. App program URLs remain separate.

Provider application buttons use the verified app login route. After login, a seeker can apply to become a provider from their account. A verified application deep link may replace this destination later.

No analytics or lead forms were added. The main actions lead to app program exploration and provider applications. Measure the subsequent app journey before claiming any increase in conversions.

## Assets and checks

The original brand symbol is retained, paired with the corrected talent-share wordmark. Existing illustrative Unsplash photos are reused. Pottery photos are by Quino Al (jsWVItac5Tw) and Sander Breneman (kJiPUr1KQSE). Other image asset sources remain recorded in the earlier project assets and source files.

All 14 pages have static HTML content, one H1, individual page metadata, and checked local links. Desktop and mobile layouts were reviewed. The mobile provider navigation and interactive communication panel were checked. Reduced-motion preferences are supported.
