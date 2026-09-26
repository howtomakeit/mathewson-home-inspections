# Mathewson Home Inspections — static site starter

A lightweight, responsive, no-build website starter for **Mathewson Home Inspections** in Ridgecrest, California. It is plain HTML/CSS/JavaScript, so it can be pushed directly to GitHub and uploaded to Hostinger’s `public_html` folder.

## Quick start

```bash
# from this folder
python3 -m http.server 8080
# open http://localhost:8080
```

No Node, PHP, database, WordPress, or build step is required.

## Hostinger deployment

1. Create a GitHub repository and push this folder.
2. In Hostinger, open **File Manager → public_html**.
3. Upload the contents of this folder (not the outer folder) or connect the repository through Hostinger’s deployment workflow.
4. Confirm the domain points to Hostinger and force HTTPS.
5. Test the phone link, email links, mobile menu, every anchor, and the logo/image paths.

The current CTA uses `tel:` and `mailto:` links so the starter works without a backend. Add a Hostinger/PHP form only if a real form is needed; do not use a fake form that silently loses leads.

## Before launch: owner verification

The old website contains valuable material, but some details conflict or may be stale. Confirm these with Russ before publishing:

- Exact business name: “Mathewson Home Inspections” vs. “Mathewson Certified Home Inspections” vs. “Ridgecrest Home Inspection Service”. Choose one public brand.
- Experience: the homepage says 35 years construction / 27 years inspection; the biography page says 33 years construction. Replace with one accurate, current statement.
- Current memberships and credentials: InterNACHI, ASHI, CREIA, USACE quality-control certification, insurance, and any money-back/report-time guarantees.
- Current pricing. The old site lists prices that may be out of date; do not migrate them without confirmation.
- Exact service area and travel surcharge policy.
- Whether mold inspection, radon information, pools/spas, specialty inspections, and pre-listing inspections are currently offered.
- Best current headshot, inspection photos, logo, and any written reviews that can legally be reused.
- HomeGauge client-report link and sample-report URLs.

## Recommended next phase

- Add a real contact form connected to a monitored business inbox.
- Add a dedicated pricing page after prices are confirmed.
- Add a reviews section with permission-based testimonials and links to Google/Yelp profiles.
- Add individual SEO pages only for services actually offered: buyer inspection, pre-listing inspection, mold, roofing/exterior, structural, plumbing, electrical, HVAC, and report delivery.
- Add Google Business Profile link, service-area details, and LocalBusiness schema after business information is verified.
- Connect Google Search Console and Analytics/Consent Mode if analytics are wanted.
- Run Lighthouse/PageSpeed and an accessibility check after final copy and imagery are in place.

## Current live-site audit — 2026-09-26

### High priority

1. **Replace the entire visual system.** The live site uses a fixed-width, dated WordPress theme with very small text, a left-side link column, generic stock imagery, and large unused space.
2. **Create one primary conversion path.** The live page shows phone/email text but no strong “schedule/request a quote” action and no working inquiry form.
3. **Remove or repair the HomeGauge login widget.** It appears on the homepage without context and presents username/password fields before a visitor has chosen to become a client. Move report access to a clearly labeled client-only link.
4. **Fix stale/placeholder content.** `/radon-information/` explicitly says it is blank placeholder information; `/your-report/` contains irrelevant legacy Mambo/GNU GPL text; the old pages have repeated boilerplate and inconsistent page naming.
5. **Reconcile factual claims.** Experience, memberships, guarantees, pricing, and scope of specialty services need owner confirmation.

### Medium priority

- Consolidate 25 indexed pages into a small, intentional information architecture.
- Replace “Welcome” H1 with a service/location/value proposition H1.
- Rewrite page titles and meta descriptions around Ridgecrest/Indian Wells Valley home inspections.
- Add descriptive image alt text; the current crawl found multiple images with missing alt text.
- Add a real About page, Services page, Buyer/Seller pages, Pricing/Quote page, Reviews page, Sample Report page, Contact page, and Client Report access page.
- Use consistent phone formatting and click-to-call behavior on mobile.
- Add a favicon, social sharing image, canonical URLs, XML sitemap, and verified LocalBusiness JSON-LD.
- Add privacy/terms pages if a contact form, analytics, or marketing tools are introduced.

### Technical notes

- HTTP and bare-domain versions redirect to `https://www.russmathewson.com/`, which is good; keep one canonical host.
- The live site is served through Cloudflare and uses Brotli compression, but several modern security headers are absent; review CSP, HSTS, referrer policy, and frame protections after confirming third-party widgets.
- The existing sitemap exposes 25 pages, including legacy pages that should be redirected or removed from the index during migration.

## Suggested repo structure

```text
index.html
styles.css
script.js
assets/
  logo.gif
  header.jpg
README.md
```
