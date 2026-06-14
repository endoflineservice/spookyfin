# Install Spookyfin

Spookyfin is installed through Jellyfin's built-in Custom CSS setting.

## Recommended install

1. Open Jellyfin in a browser.
2. Go to `Dashboard` -> `General`.
3. Find `Custom CSS code`.
4. Paste the full contents of [`../theme.css`](../theme.css).
5. Save.
6. Hard refresh the browser with `Ctrl+F5`.

This is the most reliable install because your theme will keep working even if a CDN is unavailable.

## CDN install

Paste this into Jellyfin's Custom CSS field:

```css
@import url("https://cdn.jsdelivr.net/gh/endoflineservice/spookyfin@main/theme.css");
```

If you want GitHub raw instead:

```css
@import url("https://raw.githubusercontent.com/endoflineservice/spookyfin/main/theme.css");
```

## Use the library images

1. Download or clone this repository.
2. Open Jellyfin.
3. Go to the library you want to customize.
4. Use `Edit Images`.
5. Upload a matching file from [`../assets/library-images`](../assets/library-images).

Suggested mapping:

| Jellyfin library | File |
| --- | --- |
| Collections | `assets/library-images/collections.png` |
| Movies | `assets/library-images/movies.png` |
| Shows | `assets/library-images/tv-shows.png` |
| Music | `assets/library-images/music.png` |
| Anime | `assets/library-images/anime.png` |
| Cartoons | `assets/library-images/cartoons.png` |
| Audio Books | `assets/library-images/audio-books.png` |
| ASMR | `assets/library-images/asmr.png` |
| Kids | `assets/library-images/kids.png` |
| Photos | `assets/library-images/photos.png` |
| Music Videos | `assets/library-images/music-videos.png` |
| Playlists | `assets/library-images/playlists.png` |

## Troubleshooting

- If the theme does not appear, hard refresh with `Ctrl+F5`.
- If the web app still looks old, clear the browser cache for the Jellyfin site.
- If something looks wrong, remove the custom CSS field, save, then re-add the theme.
- If you use reverse proxies or aggressive caching, purge that cache after changing CSS.
