# liszkai-landing

Personal landing page for Dávid Liszkai, test manager at OTP Bank.

CV-complement page that sits alongside the downloadable PDF resume. Static
single-file HTML site: no build step, no framework. HTML, CSS, and a little
inline SVG.

## Structure

```
.
├── index.html                  # the whole page
├── liszkai-david-en-cv.pdf     # downloadable CV (generated from cv/cv.html)
├── cv/
│   ├── cv.html                 # CV source: edit this, then re-export the PDF
│   └── fonts/                  # fonts used by cv.html
└── assets/
    ├── og-image.jpg            # social preview image (1200×630)
    └── projects/               # project screenshots (.webp, ~1200px wide)
        └── testsuite-me.webp
```

## Updating the CV

Open `cv/cv.html` in Chrome → Print → Save as PDF (A4, margins: none,
background graphics on), and save it as `liszkai-david-en-cv.pdf` in the repo root.

## Project screenshots

Export at ~1200px wide as WebP (quality ~80), put them in `assets/projects/`,
and set `width`/`height` on the `<img>` to avoid layout shift.

## Deploy

Deployed as a static site on Netlify. Any push to `master` triggers an
automatic redeploy.

## Notes

- Fonts are loaded from Google Fonts (Ubuntu 300/400/500/700, IBM Plex Mono 400/500/600).
  Only use weights that are loaded, anything else gets synthesised by the browser.
- Favicon is an inline SVG data URI in the `<head>`, no separate file.
- Theme: dark, with a cyan accent (`#7fd6ff`). All colours live as tokens in `:root`.
