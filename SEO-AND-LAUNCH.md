# SEO and conversion plan for Zenith

Prepared 7 October 2026 from Zenith's public site and primary design/search documentation. This is a practical launch plan. No claim of current Google position, search volume, conversion uplift or revenue has been invented.

## The opportunity

The strongest starting point is a clear set of destination and charter-intent pages backed by detailed yacht inventory. A broad phrase such as “yacht charters” is geographically ambiguous and competitive. Visitors searching for a specific country, island, occasion or vessel have a more defined need. Prioritize those journeys, then grow broader visibility through useful content and authority.

## Page-to-search map

These are recommended targets, not measured keyword volumes or verified current rankings.

| Search intent | Existing destination URL to retain | What the page must answer |
| --- | --- | --- |
| Yacht rental Singapore; yacht charter Singapore | `/sg/en/` | Marinas, fleet, group capacity, inclusions, quote process, FAQs |
| Singapore private yacht rental and specific yacht names | `/sg/en/our-fleet/` and each `/sg/en/yachts/.../` page | Vessel specifications, real gallery, detailed rates, charter duration and exclusions |
| Yacht charter Malaysia; private yacht rental Malaysia | `/my/en/` | Operating destinations, local fleet and enquiry options |
| Langkawi yacht charter; Penang yacht rental; Johor yacht charter | Existing `/my/en/discover/.../` routes | The specific departure area, routes, relevant yachts and useful local guidance |
| Phuket yacht charter; Thailand private yacht charter | `/th/en/` | Phuket/Andaman context, available yachts, route choices, duration and season considerations |
| Phi Phi private yacht charter; Phang Nga Bay yacht charter | Existing `/th/en/discover/.../` routes | What the itinerary involves, relevant yachts and package-specific costs |
| Corporate yacht charter Singapore | `/sg/en/experiences/corporate-team-bonding-events/` | Capacity, event setup, catering choices, logistics and enquiry requirements |
| Yacht birthday party Singapore | `/sg/en/experiences/yacht-birthday-party-specials/` | Suitable vessels, guest numbers, package options and booking process |
| Yacht wedding/proposal Singapore | `/sg/en/experiences/yacht-wedding-proposals-singapore/` | Occasion-specific setup, itinerary and planning details |

Do not publish near-identical location pages with only the place name changed. Existing destination guides should be expanded with verified local information, actual routes and useful original photos. Do not invent departure marinas, prices, season guarantees or local offices.

## Implemented in the redesign

- Crawlable, static HTML pages. Primary content and yacht cards do not depend on a JavaScript API response.
- One primary heading on each generated page, meaningful page titles, descriptions and breadcrumbs.
- Original URL paths retained wherever content was captured. Relative `index.html` links make the pitch portable.
- Descriptive links between destination hubs, inventory, individual yacht pages and experiences.
- `TravelAgency`, `WebPage` and `BreadcrumbList` JSON-LD using published business information. No fabricated rating, review count, product availability or Offer schema.
- Image dimensions on optimized local assets, lazy loading below the fold and a prioritized hero image.
- A sitemap, mobile layouts, native semantic controls and reduced-motion support.
- Noindex on the pitch. Canonicals point to Zenith's real domain, not to the pitch host.

## Before production: preserve existing SEO

1. Export all live CMS URLs and compare them with `research/content-map.json`. Add pages that are not reachable through public navigation. Check downloadable brochures and old language variants separately.
2. Export Search Console landing-page performance and backlinks before migration. Preserve URLs with existing traffic or links. If a URL changes, use a direct permanent server redirect to the relevant replacement, not the homepage.
3. Check the older `zenithyachtcharters.com.sg` domain. Search results still surfaced older .com.sg yacht pages during this research; verify current redirects and canonical behavior directly before choosing any migration rules. This search observation does not establish present server behavior.
4. Compare repeated news and legal content across root, Singapore, Malaysia and Thailand. Choose the appropriate canonical for genuinely duplicate pages after editorial review. Do not indiscriminately canonicalize different regional content to the root.
5. Keep the private/noindex pitch separate. Only on the approved production build, use the generator in the downloadable full source pack and run `ZENITH_PRODUCTION=1 python build.py`, then verify that no production page retains preview noindex rules. Review canonicals, sitemap and robots rules on the actual domain. Keep all staging copies noindex.
6. Test real responses for every important route, missing-page 404 behavior, image loading and redirects. Preserve the actual domain and existing DNS until launch is approved.
7. Measure Core Web Vitals with real-user data after launch. Local visual checks are not a Lighthouse score or evidence of real-user performance.
8. Connect Search Console, submit the production sitemap and inspect representative home, country, yacht and experience URLs. Monitor indexing and traffic after the move.

## First 30 days after launch

- **Week 1:** Confirm indexing, canonical/redirect correctness, phone and WhatsApp handoffs, form delivery if a backend is added, and conversion event definitions. Fix current/expired pricing conflicts with Zenith.
- **Week 2:** Strengthen Singapore, Phuket/Thailand and Langkawi pages with verified answers customers ask before booking. Surface route durations, inclusions, marina access and package limits where those facts are confirmed.
- **Week 3:** Improve relevant internal links from existing guides and news into country, experience and yacht pages. Remove thin duplicates only after assessing traffic and redirect needs. Update the real Google Business Profile using the correct existing business details.
- **Week 4:** Review Search Console queries and landing pages alongside actual enquiries and booked revenue. Prioritize pages getting impressions but poor click-through, and pages receiving visits but few qualified leads. Request honest customer reviews after completed charters; do not purchase or fabricate them.

Rankings develop over time and depend on competition, content, links and local relevance. A redesigned interface alone cannot guarantee a top ranking.

## Conversion strategy and measurement

The design reduces the steps between browsing and an enquiry: a visible destination/guest finder, comparable yacht cards, package details near an enquiry action, and a persistent mobile enquiry button. The message composer captures useful charter context before passing the visitor to Zenith's existing WhatsApp or email.

Measure the full sequence:

1. Destination/fleet visit.
2. Yacht detail view.
3. Enquiry open.
4. WhatsApp/email handoff.
5. Enquiry actually received and qualified by the charter team.
6. Deposit/booking completed, plus booked value.

The last two need CRM or booking-system data. Do not count a WhatsApp click as a confirmed booking. Compare before and after using consistent traffic sources, device mix, seasonality and attribution. A/B-test the hero CTA and enquiry friction once the baseline is reliable. Do not promise an unmeasured percentage improvement.

## Design references and evidence

- [OMAYA Yachts on Awwwards](https://www.awwwards.com/sites/omaya-yachts): Honorable Mention, 20 October 2025. Reference for immersive, spacious yacht presentation. Award recognition is not proof of conversion performance.
- [Y.CO](https://y.co/): reference for photography-led brand storytelling, charter discovery and clear enquiry access.
- [Burgess charter experience](https://www.burgessyachts.com/en/charter-a-yacht): reference for destination and yacht browsing with detailed specifications.
- [CreateSwift's Pattaya Yacht Charters case study](https://createswift.com/portfolio/pattayayacht): describes transparent fleet presentation and a pre-qualifying enquiry flow. It does not establish an independently verified conversion-rate lift or an industry “best converter.”
- [Google: site moves with URL changes](https://developers.google.com/search/docs/crawling-indexing/site-move-with-url-changes): URL mapping, redirects and migration monitoring.
- [Google: changing hosting without URL changes](https://developers.google.com/search/docs/crawling-indexing/site-move-no-url-changes): staging and production accessibility checks.
- [Google: canonical URLs](https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls): duplicate-page consolidation.
- [Google: SEO for developers](https://developers.google.com/search/docs/fundamentals/get-started-developers): crawlable content, metadata and structured data foundations.

Public data does not provide a credible, apples-to-apples ranking of which yacht site converts best. These references inform the design; actual Zenith performance must be measured after launch.

## Media handoff

The pitch combines optimized local copies with original Zenith image URLs where downloads were blocked. Before production, obtain the original media library and replace remote dependencies with correctly sized files on the production domain. Confirm image rights, alt text, intrinsic dimensions and mobile loading performance.

The GitHub edition serves optimized photos from the public pitch image host. Before a production migration, copy the media from the full source pack to the production domain and replace those asset URLs.
