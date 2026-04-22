# liszkai-landing

Personal landing page for Dávid Liszkai — software tester, acting test manager.

CV-complement page that sits alongside the downloadable PDF resume. Built as a
static single-file HTML site. No build step, no framework — just HTML, CSS, and
a sprinkle of inline SVG.

## Structure

```
.
├── index.html                          # the whole page
├── david-liszkai-cv.pdf                # downloadable CV
├── og-image.png                        # social preview image (1200×630)
└── assets/
    └── projects/                       # project screenshots
        ├── recipe-collector-index.png
        └── testsuite-me.png
```

## Deploy

Deployed as a static site on Netlify. Any push to `main` triggers an
automatic redeploy.

## Notes

- Fonts are loaded from Google Fonts (Ubuntu, IBM Plex Mono).
- Favicon is an inline SVG data URI in the `<head>` — no separate file.
- Theme: dark, with a cyan accent (`#7fd6ff`).
