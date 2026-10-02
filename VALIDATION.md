# Redesign validation — 2 October 2026

## Completed

- Isolated local branch: `website-redesign-2026`, based on
  `cb788a3df0de3f0c7a2f51c9c7809321b665b0a6` from `main`.
- Jekyll 4.3.2 build with jekyll-seo-tag 2.8.0: passed.
- All four compiled pages were checked for internal URLs, fragment targets,
  stylesheet paths, image paths and every `srcset` image: passed.
- All 13 supplied About paragraphs were checked against the rendered output.
  Scientific wording is preserved, with British English spelling adjustments.
- All seven People profiles, education entries and research interests remain.
  The author's current affiliation is updated to Wiko. Student classifications
  are retained from the source; their current status was not independently audited.
- Every page has one `h1`, one document title, unique element IDs and one
  active navigation item. Heading levels are consecutive. Images have
  meaningful alternative text and explicit dimensions. The map has a title.
- Keyboard navigation is native HTML, with a skip link and visible focus
  styles. No JavaScript is needed for navigation.
- Text contrast against the page background: ink 13.27:1, muted text 5.85:1,
  accent 7.56:1. All exceed the WCAG AA normal-text threshold.
- No rendered page loads resources from the reference website. The stylesheet
  is local, with no remote fonts, Font Awesome or global MathJax.
- SEO titles, descriptions, canonical URLs, locale, Open Graph image and JSON-LD
  were inspected in the generated HTML.
- Wiko address, fellowship dates, map marker and photograph licence were
  verified against the sources in `ASSETS.md`.
- Original image URLs remain available. New images use explicit dimensions,
  responsive source sets where needed, and JPEG optimisation.
- `git diff --check`: passed. Modified source files were inspected.

## External links

The original external URLs were checked. Five ResearchGate URLs returned
HTTP 403 to automated requests, so they are preserved and remain unverified.
The two older `jsmc-phd.de` URLs timed out; they were replaced with official
Jena university pages for Stefan Schuster and the Bioinformatics staff list.
The other checked sources responded successfully.

## Remaining checks and publishing limitation

- The cloud browser rejected localhost previews and local-file navigation.
  Desktop and mobile rendered layouts, interactive keyboard behaviour, the
  live embedded map and network/layout-shift measurements have therefore
  **not** been visually verified. Media-query code was reviewed, but that is
  not equivalent to a browser test. Review at 320, 390, 768 and 1440 px before
  merging. The handoff package includes built HTML for this review.
- The build here used Jekyll 4.3.2. The committed Gemfile uses `github-pages`
  for local reproduction with GitHub Pages dependencies; the hosted build is
  still to be checked once the branch can be pushed.
- The GitHub integration rejected remote branch creation with HTTP 403,
  “Resource not accessible by integration”. No changes have been made to
  remote `main`. No remote branch or pull request was created. A normal Git
  push also failed because this workspace has no GitHub credentials.

## Intended pull request

Title: Redesign Leonardo Oña's academic website and update Wiko contact details

The redesign replaces the externally shared CSS with an independent local
design and makes Leonardo Oña the primary identity. It adds a research-led
homepage, implements the supplied About text in British English, retains and
restyles all People profiles, and updates the Contact page to Wiko with a
licensed local photograph and the official map marker. It also optimises
portraits, improves semantic HTML and keyboard focus, preserves Jekyll SEO,
and makes unused mathematics support opt-in.

Open against `main`, leave unmerged, and report the outstanding browser/hosted
build checks and automated ResearchGate-link limitations in the description.
