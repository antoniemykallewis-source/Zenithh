# Zenith Yacht Charters: redesign concept

A complete static pitch website built from Zenith's public website on 7 October 2026. The design preserves the original logo, gold/navy/turquoise palette, published business contacts, regional destinations and yacht information.

## Open the site

The website starts at `dist/index.html`. It works on a static host, including GitHub Pages. Upload the **entire `dist` folder contents**, not only its index file, to preserve all pages and images. Links are relative so the site also works under a GitHub project subdirectory.

For development, run `npm ci` and `npm run dev`. This serves the already generated static pages. Rebuild with Python 3, Beautiful Soup 4 and Pillow using `python build.py`.

## What's included

- A new editorial homepage with the original Zenith branding and photography.
- Three destination hubs, a unified fleet finder and the original regional fleet URLs.
- 103 yacht detail pages: Singapore 60, Malaysia 14, Thailand 29.
- Original specifications, rate tables, inclusions, exclusions and package conditions.
- Destination guides, experience pages, join trips, news, FAQs and policies from the 238-page linked-content crawl.
- A short enquiry flow that prepares a message for Zenith's published WhatsApp number or opens an email draft. It does not submit bookings, charge guests, or claim a message has been delivered.
- Responsive layouts, accessible native forms/disclosures/dialogs, reduced-motion support, lazy-loaded images and descriptive page titles.
- A source URL map, asset inventory, SEO launch notes and conversion event hooks.

## Pitch status

The preview is deliberately `noindex` and uses Zenith's original-domain canonical URLs. It is a sales concept, not a production replacement for Zenith's current website. Review the launch notes before deploying to their domain.

Published yacht rates are source data, not live quotes or availability. Lemon and Peach have source tables with validity dates that have expired; these are flagged on their pages. Do not remove the flags without confirmed current pricing.

The Singapore catalogue has 60 yachts. Across the three regional catalogues the crawl identified 103 yacht records; the original homepage's separate `100+` fleet claim is preserved.

## Conversion measurement

`assets/app.js` emits `fleet_search`, `enquiry_open`, `enquiry_handoff` and `contact_click` to `window.dataLayer`. No analytics service is connected. `enquiry_handoff` means an external message composer was opened, not that a qualified lead or booking was received. Record actual leads and paid bookings in Zenith's CRM and reconcile those downstream outcomes before reporting uplift.

## Content and media

`research/content-map.json` maps original URLs to rebuilt pages. `research/fleet.json` records the extracted catalogue. `research/pages.json` and `research/details.json` are source snapshots used by the generator. `research/asset-map.json` traces optimized local images to their original source URLs.

Accessible image files have been optimized and bundled locally. Images whose download requests were blocked retain their original Zenith source URLs. Those images require internet access and continued availability on Zenith's website. Obtain the original media library from Zenith before a production migration.

Zenith's branding, text and photography remain the property of their respective owners. Their inclusion is for the requested redesign pitch. Obtain Zenith's approval before using this as their live site. No unrelated company's photos or copy have been used in the design.

## Known source boundaries

The crawl followed all unique navigable public links discovered from the homepage and the three regional English sites. It is not a CMS export. Unlinked pages, hidden inventory, untranslated locale variants, downloadable attachments and private booking data are not claimed to be migrated. Two attempted links were not usable content pages: a Cloudflare email-obfuscation endpoint and `/sg/`, whose request returned 403. The working Singapore homepage is `/sg/en/` and all 60 listed yachts were captured.

Before launch, reconcile the URL map with the CMS and Search Console, confirm all pricing and contact details, review legal pages, connect the agreed form/CRM workflow and follow `SEO-AND-LAUNCH.md`.
