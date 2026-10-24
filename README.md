# Strix Halo Stars

Minimal static landing page for Donato Capitella’s podcast about the people building local AI on AMD Strix Halo. The website is in [`docs/`](docs/); there are no build tools, package dependencies, JavaScript, analytics, or embedded third-party players.

## Preview

From this repository, run:

```sh
python3 -m http.server 8000 --bind 127.0.0.1 --directory docs
```

Open http://127.0.0.1:8000. You can also open `docs/index.html` directly.

## Content and branding

The authoritative podcast workspace is `/home/kyuz0/Documents/Projects/strix-halo-stars-podcast`. Read [`AGENTS.md`](AGENTS.md) before editing. The page currently previews episode 1 as **in production**, with no feed, player, release date, or listening-platform claims.

`docs/brand.css` mirrors the Toolboxes brand tokens from `/home/kyuz0/Documents/Projects/amd-strix-halo-gfx1151-toolboxes/docs/brand.css`. Layout and responsive rules live in `docs/styles.css`. The processor-contour artwork was generated specifically for this landing page; the episode number is real HTML, so future episodes can use new artwork and accessible text without baking metadata into images. The generated PNG source is retained in `artwork/`; the page uses a compressed WebP in `docs/assets/`.

## When episode 1 is published

Update the status and description from the approved publication package, then add the actual audio-host/player and RSS/listening links. Set the canonical URL, absolute Open Graph image URL, and social preview metadata when the website’s public URL is decided. Keep every asset path relative and verify the site at both a domain root and a GitHub Pages project subpath.

## Hosting

This is ready for GitHub Pages using **Deploy from a branch**, branch `main`, folder `/docs`, once the files have been committed and pushed and publication is authorized. `docs/.nojekyll` keeps the static files unprocessed. No deployment or custom domain is configured by this change.
