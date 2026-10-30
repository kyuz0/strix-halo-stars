# Strix Halo Stars — landing page

This repository contains only the public static website. The actual podcast content, editorial instructions, episode status, research, production records, and publication decisions live in **`/home/kyuz0/Documents/Projects/strix-halo-stars-podcast`**.

Before changing content, read that repository’s `AGENTS.md`, `MEMORIES.md`, `planning/STATUS.md`, and the relevant episode’s `README.md`. Treat them as the source of truth. Do not copy private production files, recordings, contacts, or unpublished transcripts into this repository.

- Keep the site static and buildless in `docs/`, suitable for GitHub Pages with `/docs` as its source. Use relative asset paths so project-subpath hosting works. Do not add a framework or backend for routine page work.
- Preserve the Toolboxes visual identity: charcoal `#171a1d`, warm gold `#f2b544`, off-white text, restrained monospace details, and a minimal layout. The reference is `/home/kyuz0/Documents/Projects/amd-strix-halo-gfx1151-toolboxes/docs/` and https://strix-halo-toolboxes.com/.
- Donato Capitella creates and hosts the show. In episode 1, Usman Pirzada from AMD introduces and interviews Donato throughout. Keep this distinction accurate.
- Episode 1 was published on RSS.com on 30 October 2026 at 17:55:13 UTC. The website uses its episode-specific dark player, published details, RSS feed and episode cover. Apple Podcasts, Spotify and Amazon Music are still processing in the latest dashboard screenshot; add their buttons when public links work. Never invent a release schedule, subscriber count, or availability.
- Include the short AMD sponsorship acknowledgement. Do not present this community podcast or Toolboxes as official AMD products.
- Preserve the established Toolboxes, YouTube, GitHub, LinkedIn, and Buy Me a Coffee destinations. Keep authored copy in Donato’s first person.
- Check desktop and mobile layout, keyboard focus, internal navigation, and asset loading after visual changes. Preserve reduced-motion support.
- Publishing, pushing to GitHub, changing Pages settings, or adding a custom domain requires the user’s instruction; creating the local page is not publication authorization.

Use unpadded public episode numbers: “Episode 1”, “Episode 2”, and so on; banner numerals should be “1”, “2”, etc.

Selected visual identity: `artwork/chip-constellation.png`, combining a gold processor outline, three connected stars and flowing gold/grey traces. Use `artwork/banner-wide.png` for the titled wide version and `docs/assets/cover-square-3000.jpg` for the titled square cover. Preserve the original generated square source; the 3000-pixel JPEG is a resampled export.

Title typography: keep “STARS” gold, with the same font size and capital-letter height as “STRIX HALO”. Do not enlarge it or stretch it to the first line’s width. Apply this to wide and square artwork.

Public-facing copy should contain only useful listener information. Use “Coming soon” for an unreleased episode; keep editing progress, production status and internal workflow details out of the public page. Avoid repeating the same availability message in multiple places.

Layout correction, 24 October 2026: follow the actual Toolboxes drafting-grid background and restrained type scale. Keep page typography compact (current title cap: 48px desktop, 30–32px phones; body 15–16px). Do not restore a giant two-line hero or a full-width square hero image on phones. The episode artwork MUST remain square at all viewport sizes; use `docs/assets/cover-square.webp`, not the wide banner. Keep the wide file only as a separate artwork export. Check mobile touch emulation and visual density as well as overflow; a page can have no horizontal overflow and still scale badly.
