# talent-share website

A content-led, statically generated marketing website. Marketplace listings, teacher profiles, bookings, prices, dates, and account workflows remain at https://app.talent-share.com/.

## Run locally

Requires Python 3. No third-party Python packages or JavaScript build tools are required.

```sh
python3 build.py
python3 -m http.server 4173 --directory dist
```

Open http://localhost:4173/. Serve the `dist` directory; opening HTML files directly will not resolve root-relative links.

## Edit

- `build.py`: all page content and shared page components.
- `src/style.css`: responsive layout, colour, typography, animation.
- `src/site.js`: mobile menu, communication tabs, FAQ search, subject filters, reduced-motion-aware reveal animation.
- `assets`: local imagery and original talent-share logo.
- `seo-map.json`: page titles, descriptions, and primary keyword targets.

`build.py` regenerates the 14 HTML pages, sitemap, robots file, and the separate website-copy document in the parent outputs folder. All primary content renders without JavaScript. JavaScript enhances navigation and the illustrative product interactions. Google Fonts supplies DM Sans and Manrope, with local system-font fallbacks.

## Launch on the existing domain

The current build is a private review version with `noindex,nofollow` and a disallow-all robots file. It is not a replacement of the live www.talent-share.com site.

When the content is approved and hosting is ready:

```sh
SITE_ORIGIN=https://www.talent-share.com PRODUCTION=1 python3 build.py
```

This sets the production canonical URLs and sitemap and enables indexing. Publish the resulting `dist` files on the chosen static host. Do not enable indexing for a second public copy at another hostname.

Preserve the existing legal/privacy content and `/legal` route when migrating. The design links to the current legal page; it deliberately does not invent replacement legal terms. Preserve appropriate redirects from existing routes such as `/about-us` to `/about/` and `/become-provider` to `/teach/`. Confirm any contact-page migration and retain links that are already indexed. The app and its program URLs must remain independent.

The teacher CTA uses the verified `/login` app route. After sign-in, teachers apply from their account. Replace this destination with a verified application deep link if the app supports one.

## Content boundaries

Product facts are based on the supplied talent-share Website Feature Brief. Editorial subject guides describe how to choose a program and are not claims about current program inventory. All photos are illustrative. Product interface drawings and example messages are labelled as illustrations, not live app screenshots.

No dummy listings, provider bios, testimonials, ratings, learner counts, revenue claims, fee percentages, payout promises, certificates, or app-store links are included.

## Verification

All 14 routes checked for one H1, a title, a meta description, existing local assets, and valid internal links. JavaScript syntax checked. Desktop 1280px and mobile 390px layouts inspected, with no horizontal overflow on the tested home, teaching, and FAQ pages. Mobile menu, FAQ search, subject filters, and communication panel switching verified in the browser. Reduced-motion preferences are respected.

## Content structure

The homepage now follows seeker need, live-learning value, subject choice, booking confidence, the program experience, and next steps. The provider page has a separate narrative about discovery and program management. Audience terms are providers and seekers; offerings are programs. See CONTENT-STRATEGY.md for the role of each page.
