# Strix Halo Stars

Minimal static landing page for Donato Capitella’s podcast about the people building local AI on AMD Strix Halo. The website is in [`docs/`](docs/); there are no build tools, package dependencies or first-party JavaScript. Episode playback uses RSS.com’s embedded player.

## Preview

From this repository, run:

```sh
python3 -m http.server 8000 --bind 127.0.0.1 --directory docs
```

Open http://127.0.0.1:8000. You can also open `docs/index.html` directly.

## Content and branding

The authoritative podcast workspace is `/home/kyuz0/Documents/Projects/strix-halo-stars-podcast`. Read [`AGENTS.md`](AGENTS.md) before editing. The homepage keeps show-level subscription links near the introduction and lists episodes as compact rows. Each entire row, including its cover and title, links to the listening page. Episode 1’s listening page is [`docs/episodes/1/index.html`](docs/episodes/1/index.html), with its episode-specific RSS.com player, collapsed notes/chapters and audio/transcript link. Apple Podcasts and Pocket Casts use Donato’s exact show URLs; Spotify is explicitly a search destination until its direct show URL is available.

`docs/brand.css` mirrors the Toolboxes brand tokens from `/home/kyuz0/Documents/Projects/amd-strix-halo-gfx1151-toolboxes/docs/brand.css`. Layout and responsive rules live in `docs/styles.css`. The selected artwork combines a processor, a three-star constellation and flowing gold/grey traces. The hero uses the text-free square illustration; the homepage’s episode row uses a small square cover. On the separate episode page, artwork appears only inside the player. Generated PNG sources are retained in `artwork/`; the page uses compressed WebPs in `docs/assets/`. Episode numbering stays in HTML metadata rather than being baked into show artwork. The original processor-contour PNG is retained as an earlier source.

## Artwork exports

- [Wide titled banner](artwork/banner-wide.png): 2172×724 PNG (3:1).
- [Square podcast cover](docs/assets/cover-square-3000.jpg): 3000×3000 opaque RGB JPEG, with the podcast title.
- [Text-free chip and constellation](artwork/chip-constellation.png): 1254×1254 PNG.

The square cover was generated at 1254×1254; the 3000-pixel export is a high-quality Lanczos resample, not a claim of native 3000-pixel generation. Its original is preserved as `artwork/cover-square-source.png`. The show and episode audio are hosted on RSS.com.

## Publishing episodes

Follow the podcast repository’s `docs/PUBLISHING.md` and episode publication record. Use the actual RSS.com episode embed from Share → Embed → Episode, preserving the episode ID so older entries keep playing the intended release. Keep audio on RSS.com and copy only public-ready artwork and copy here. For each release, add one compact homepage row and a dedicated `docs/episodes/N/index.html` page. Subscription links stay at show level, and the homepage contains no embedded players. Use relative paths for local assets and verify desktop/mobile layout, homepage-to-episode/back navigation, keyboard access, chapters and playback before pushing.

## Hosting

The site is published at https://strix-halo-stars.com/ using GitHub Pages, branch `main`, folder `/docs`. `docs/.nojekyll` keeps the static files unprocessed. Preserve `docs/CNAME` and verify the live page after pushing.
