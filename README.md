# Strix Halo Stars

Minimal static landing page for Donato Capitella’s podcast about the people building local AI on AMD Strix Halo. The website is in [`docs/`](docs/); there are no build tools, package dependencies or first-party JavaScript. Episode playback uses RSS.com’s embedded player.

## Preview

From this repository, run:

```sh
python3 -m http.server 8000 --bind 127.0.0.1 --directory docs
```

Open http://127.0.0.1:8000. You can also open `docs/index.html` directly.

## Content and branding

The authoritative podcast workspace is `/home/kyuz0/Documents/Projects/strix-halo-stars-podcast`. Read [`AGENTS.md`](AGENTS.md) before editing. Episode 1 was published on RSS.com on 30 October 2026. The page includes its published title, date, duration, episode-specific dark player with its cover, chapter list, public transcript/episode link and RSS subscription link. Directory buttons can be added once their public URLs work; directory processing does not block website publication.

`docs/brand.css` mirrors the Toolboxes brand tokens from `/home/kyuz0/Documents/Projects/amd-strix-halo-gfx1151-toolboxes/docs/brand.css`. Layout and responsive rules live in `docs/styles.css`. The selected artwork combines a processor, a three-star constellation and flowing gold/grey traces. The hero uses the text-free square illustration; Episode 1’s player displays its topic-specific square cover; no second episode thumbnail is shown. Generated PNG sources are retained in `artwork/`; the page uses compressed WebPs in `docs/assets/`. Episode numbering stays in HTML metadata rather than being baked into show artwork. The original processor-contour PNG is retained as an earlier source.

## Artwork exports

- [Wide titled banner](artwork/banner-wide.png): 2172×724 PNG (3:1).
- [Square podcast cover](docs/assets/cover-square-3000.jpg): 3000×3000 opaque RGB JPEG, with the podcast title.
- [Text-free chip and constellation](artwork/chip-constellation.png): 1254×1254 PNG.

The square cover was generated at 1254×1254; the 3000-pixel export is a high-quality Lanczos resample, not a claim of native 3000-pixel generation. Its original is preserved as `artwork/cover-square-source.png`. The show and episode audio are hosted on RSS.com.

## Publishing episodes

Follow the podcast repository’s `docs/PUBLISHING.md` and episode publication record. Use the actual RSS.com episode embed from Share → Embed → Episode, preserving the episode ID so older entries keep playing the intended release. Keep audio on RSS.com and copy only public-ready artwork and copy here. Use relative paths for local assets and verify desktop/mobile layout, keyboard access, chapters and playback before pushing.

## Hosting

The site is published at https://strix-halo-stars.com/ using GitHub Pages, branch `main`, folder `/docs`. `docs/.nojekyll` keeps the static files unprocessed. Preserve `docs/CNAME` and verify the live page after pushing.
