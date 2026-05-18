# Ivan Vdovin - Portfolio

Static, recruiter-facing portfolio site for Project / Delivery / Program Manager positioning.

## Design

Light editorial direction: warm paper background, near-black ink, a single accent,
generous whitespace, and a sans + monospace type pairing (Inter + IBM Plex Mono).

The "delivery system" idea is kept as the structural spine - signal, intervention,
outcome - rather than a literal dashboard. One dark "Approach" band and a dark footer
give the page rhythm; everything else is light and divided by hairline rules.

Design rationale is documented in `design-variants.html` (kept as internal design notes,
not linked from the public navigation).

## Languages

The site is bilingual. English is the default; Russian pages use a `-ru` suffix.
An `EN / RU` switcher in the navigation links the two, and each page declares
`hreflang` alternates. When editing content, update an English page and its
`-ru` counterpart together.

## Files

English:

- `index.html` - homepage
- `case-studies.html` - case files, in STAR format
- `resume.html` - web resume (print-friendly)
- `design-variants.html` - design notes / rationale (English only)

Russian:

- `index-ru.html`, `case-studies-ru.html`, `resume-ru.html`

Shared:

- `styles.css` - shared styling
- `main.js` - scroll-reveal progressive enhancement

## Stack

Plain HTML, CSS, and one small JavaScript file. No build step. Fonts load from
Google Fonts; everything else is self-contained. The site works without JavaScript
(reveal animations simply do not run).

## Deployment

Deploy as static files - Cloudflare Pages or GitHub Pages both work. No build command
is required; serve the directory as-is.

To preview locally:

    python3 -m http.server 8000
