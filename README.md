# Strix Halo Stars

Minimal static landing page for Donato Capitella’s podcast about the people building local AI on AMD Strix Halo. The website is in [`docs/`](docs/); there are no build tools, package dependencies, JavaScript, analytics, or embedded third-party players.

## Preview

From this repository, run:

```sh
python3 -m http.server 8000 --bind 127.0.0.1 --directory docs
```

Open http://127.0.0.1:8000. You can also open `docs/index.html` directly.

## Content and branding

The authoritative podcast workspace is `/home/kyuz0/Documents/Projects/strix-halo-stars-podcast`. Read [`AGENTS.md`](AGENTS.md) before editing. The page currently previews episode 1 as **coming soon**, with no feed, player, release date, or listening-platform claims.

`docs/brand.css` mirrors the Toolboxes brand tokens from `/home/kyuz0/Documents/Projects/amd-strix-halo-gfx1151-toolboxes/docs/brand.css`. Layout and responsive rules live in `docs/styles.css`. The selected artwork combines a processor, a three-star constellation and flowing gold/grey traces. The hero uses the text-free square illustration; the episode preview uses the titled square cover. Generated PNG sources are retained in `artwork/`; the page uses compressed WebPs in `docs/assets/`. Episode numbering stays in HTML metadata rather than being baked into show artwork. The original processor-contour PNG is retained as an earlier source.

## Artwork exports

- [Wide titled banner](artwork/banner-wide.png): 2172×724 PNG (3:1).
- [Square podcast cover](docs/assets/cover-square-3000.jpg): 3000×3000 opaque RGB JPEG, with the podcast title.
- [Text-free chip and constellation](artwork/chip-constellation.png): 1254×1254 PNG.

The square cover was generated at 1254×1254; the 3000-pixel export is a high-quality Lanczos resample, not a claim of native 3000-pixel generation. Its original is preserved as `artwork/cover-square-source.png`. No upload to a podcast service has been performed.

## When episode 1 is published

Update the status and description from the approved publication package, then add the actual audio-host/player and RSS/listening links. Set the canonical URL, absolute Open Graph image URL, and social preview metadata when the website’s public URL is decided. Keep every asset path relative and verify the site at both a domain root and a GitHub Pages project subpath.

## Hosting

This is ready for GitHub Pages using **Deploy from a branch**, branch `main`, folder `/docs`, once the files have been committed and pushed and publication is authorized. `docs/.nojekyll` keeps the static files unprocessed. No deployment or custom domain is configured by this change.
