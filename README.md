# nelsonlab website

A static site for the Nelson Lab, built with [Astro](https://astro.build/) and [Tailwind CSS](https://tailwindcss.com/), and deployed to Cloudflare Pages.

## Structure

- `src/pages/` — One file per page route. Markdown pages use `src/layouts/Layout.astro` for the site chrome.
- `src/components/` — Reusable components (`Header.astro`, `Footer.astro`).
- `src/data/` — Editable data files:
  - `site.json` — Site title, tagline, institution, and navigation links.
  - `people.json` — Lab members and alumni.
- `src/styles/global.css` — Tailwind entry point.
- `public/` — Static assets, including `favicon.svg` and Cloudflare `_redirects`.

## Development

```bash
npm install
npm run dev
```

Open the local URL shown in the terminal to preview changes.

## Editing content

- **Navigation** — Edit `src/data/site.json`.
- **Home page hero** — Edit `src/pages/index.astro`.
- **People** — Edit `src/data/people.json`.
- **Projects, Publications, Resources, Learning R** — Edit the corresponding Markdown file in `src/pages/`.
- **Global styles** — Edit `src/styles/global.css` or add Tailwind utility classes directly in components and pages.

## Deployment

The site is built and deployed from the `main` branch via Cloudflare Pages.

Build settings:

- **Build command:** `npm run build`
- **Build output directory:** `dist`
- **Root directory:** `/`

## Custom domain

`nelsonlab.science` is configured as the primary custom domain. `www.nelsonlab.science` redirects to the apex domain via `public/_redirects`.
