# hack-timeline

Single-page timeline portfolio for Arun. All HTML, CSS, and JS live in `index.html` — no build step.

## Deploy

Cloudflare Pages via **direct upload** (not GitHub-connected):

```
wrangler pages deploy /Users/arun02139/hack-timeline --project-name hack-timeline
```

Git push alone does NOT publish. Always run wrangler after pushing.

## Structure

- `index.html` — everything: data, styles, renderer
- `*.png / *.jpg / *.jpeg` — project images referenced by filename in the DATA block
- `og-image.jpg` — OpenGraph preview image for link sharing

## Editing content

The `DATA` object near the top of `index.html` drives everything. Edit that block to add/remove projects, badges, or career steps. The renderer below it builds the page from DATA automatically.

## Responsive design

- Desktop: default styles (no media query)
- Mobile: `@media (max-width: 768px)` block — do not change desktop styles when fixing mobile
- Print: `@media print` block
