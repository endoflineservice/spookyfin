# Spookyfin

[![Jellyfin custom CSS](https://img.shields.io/badge/Jellyfin-custom%20CSS-00e5ff?style=for-the-badge)](https://jellyfin.org/)
[![Material You inspired](https://img.shields.io/badge/Material%20You-inspired-101b20?style=for-the-badge)](https://m3.material.io/)
[![License: MIT](https://img.shields.io/badge/License-MIT-a9f7ff?style=for-the-badge)](LICENSE)

![Spookyfin preview](docs/screenshots/home-preview.png)

Spookyfin is a fast, rounded, cyan-accent Jellyfin custom CSS theme inspired by Material You, Android-style surfaces, and spooky-cute media library art.

It is built for people searching for:

`jellyfin theme`, `jellyfin custom css`, `material you jellyfin`, `android jellyfin theme`, `jellyfin dark theme`, `jellyfin library images`, `spooky jellyfin theme`, `media server theme`

## Features

- Material You inspired dark UI with bright cyan accent color.
- Rounded cards, buttons, dialogs, menus, and library tiles.
- Cleaner home rows with tinted card surfaces instead of heavy borders.
- Centered poster hover actions and better padding for badges and long titles.
- Safe rounded styling that avoids overriding Jellyfin's internal poster, blurhash, lazy-load, and card click layers.
- Included spooky-cute library artwork for Movies, Shows, Music, Collections, Anime, Cartoons, Audio Books, ASMR, Kids, Photos, Music Videos, Playlists, and an extra X library image.

## Who This Is For

Use Spookyfin if you want Jellyfin to feel more like a modern Android media app: rounded, fast, high contrast, touch friendly, and still clean enough for daily couch use.

## Install

1. Open Jellyfin.
2. Go to `Dashboard` -> `General`.
3. Find `Custom CSS code`.
4. Paste the contents of [`theme.css`](theme.css).
5. Save, then hard refresh your browser with `Ctrl+F5`.

Optional CDN install:

```css
@import url("https://cdn.jsdelivr.net/gh/endoflineservice/spookyfin@main/theme.css");
```

More details are in [docs/INSTALL.md](docs/INSTALL.md).

## Screenshots

![Home preview](docs/screenshots/home-preview.png)

![Library art preview](docs/screenshots/library-art-preview.png)

## Included Library Images

The full-size PNGs are in [`assets/library-images`](assets/library-images).

| Library | Image |
| --- | --- |
| Collections | <img src="assets/library-images/collections.png" alt="Collections library art" width="220"> |
| Movies | <img src="assets/library-images/movies.png" alt="Movies library art" width="220"> |
| TV Shows | <img src="assets/library-images/tv-shows.png" alt="TV Shows library art" width="220"> |
| Music | <img src="assets/library-images/music.png" alt="Music library art" width="220"> |
| Anime | <img src="assets/library-images/anime.png" alt="Anime library art" width="220"> |
| Cartoons | <img src="assets/library-images/cartoons.png" alt="Cartoons library art" width="220"> |
| Audio Books | <img src="assets/library-images/audio-books.png" alt="Audio Books library art" width="220"> |
| ASMR | <img src="assets/library-images/asmr.png" alt="ASMR library art" width="220"> |
| Kids | <img src="assets/library-images/kids.png" alt="Kids library art" width="220"> |
| Photos | <img src="assets/library-images/photos.png" alt="Photos library art" width="220"> |
| Music Videos | <img src="assets/library-images/music-videos.png" alt="Music Videos library art" width="220"> |
| Playlists | <img src="assets/library-images/playlists.png" alt="Playlists library art" width="220"> |
| X Library | <img src="assets/library-images/x-library.png" alt="Extra X library art" width="220"> |

## Customize

Most of the personality lives in the first `:root` block of [`theme.css`](theme.css).

Change these variables to recolor the theme:

```css
:root {
  --my-primary: #00e5ff;
  --my-primary-2: #a9f7ff;
  --my-primary-container: #006b80;
  --my-bg: #071014;
  --my-surface: #101b20;
}
```

## Notes

- This is a Jellyfin custom CSS theme, not a server plugin.
- Tested against Jellyfin 10.11.x web UI.
- The theme intentionally keeps media image/click internals light so posters, libraries, and playback controls keep behaving like stock Jellyfin.
- Always keep a copy of your old custom CSS before replacing it.
- If posters look stale after installing, hard refresh the browser or clear Jellyfin web cache.

## License

MIT for the CSS, docs, and bundled artwork in this repository. See [LICENSE](LICENSE).
