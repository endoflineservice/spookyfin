# Jellyfin Enhanced Setup Notes

Spookyfin works without Jellyfin Enhanced. Enhanced is optional, but it is a good match when you want top tabs like `Watchlist` and `Calendar`, a richer pause screen, bookmarks, and Radarr/Sonarr release pages.

The best setup is intentionally light: let Spookyfin control the theme colors and layout, then use Jellyfin Enhanced for the extra pages and media tools.

## Install Order

1. Install Spookyfin's `theme.css`.
2. Install `spookyfin-helper.js` if you want the accent picker, custom rows, and image rehydration repairs.
3. In Jellyfin, open `Dashboard` -> `Plugins` -> `Repositories`.
4. Add the Jellyfin Enhanced repository for Jellyfin 10.11:

   ```text
   https://raw.githubusercontent.com/n00bcodr/jellyfin-plugins/main/10.11/manifest.json
   ```

5. Install `Jellyfin Enhanced` from the plugin catalog.
6. Restart Jellyfin.
7. Install `File Transformation` if it is available in the catalog. The Enhanced project recommends it to avoid web-file permission issues.
8. Open `Dashboard` -> `Plugins` -> `Jellyfin Enhanced`.
9. Enable only the pages and features you actually use.

## Recommended Companion Plugins

| Plugin | Recommendation | Why |
| --- | --- | --- |
| `File Transformation` | Install first | Helps Enhanced make web-client changes cleanly across Docker, Windows, and Linux installs. |
| `Custom Tabs` | Install if using top tabs | Best way to add `Watchlist`, `Calendar`, requests, or hidden-content pages to navigation. |
| `Plugin Pages` | Install if Enhanced asks for it | Lets plugin pages behave like first-class Jellyfin pages. |
| `Kefin Tweaks` | Optional | Useful for extra watchlist features, but skip it if you do not use Seerr/watchlist tooling. |
| `Intro Skipper` | Optional | Only needed if you enable Enhanced intro/outro auto-skip. |

## Recommended Enhanced Settings

| Area | Suggested setting | Notes |
| --- | --- | --- |
| `Overview` | Confirm service status is green | Fix plugin/dependency issues before styling anything. |
| `Display` | Keep global color/theme overrides off | Spookyfin should own the accent colors, backgrounds, buttons, and cards. |
| `Playback` | Enable `Custom Pause Screen` and `Bookmarks` | Spookyfin styles the spotlight/pause buttons to match the theme. |
| `Playback` | Enable `Tab-switch actions` | Good quality-of-life feature for web/app playback. |
| `Playback` | Leave intro skip off unless `Intro Skipper` is installed | Avoids dead controls. |
| `Pages` | Add `Watchlist` and `Calendar` as custom tabs | These are the cleanest top-nav additions for Spookyfin. |
| `*arr` | Connect Radarr and Sonarr before using Calendar | The calendar needs those services to show useful release data. |
| `Seerr` | Configure only if you use Jellyseerr/Overseerr | Otherwise requests/watchlist sync can stay off. |
| `Extras` | Use `Random Button` if you like discovery | It fits well as a compact top-bar action. |
| `Visual tags` | Keep badges light | Too many badges make poster rows crowded. |

## Suggested Top Tabs

Start with this order:

1. `Home`
2. `Favorites`
3. `Watchlist`
4. `Calendar`

That keeps the header compact and matches the Spookyfin screenshots. Add more tabs only if you use them every day.

## Calendar Notes

The calendar is most useful after Radarr and Sonarr are connected in the Enhanced `*arr` settings. If it opens but looks empty:

1. Confirm Radarr/Sonarr URLs and API keys are saved.
2. Confirm Enhanced can reach those services from the Jellyfin server or container.
3. Check whether the calendar filters are hiding event types.
4. Restart Jellyfin after changing plugin dependencies.
5. Hard refresh the browser with `Ctrl+F5`.

## Styling Notes

Spookyfin includes CSS for:

- Enhanced panel cards and tabs.
- Calendar buttons, filter chips, event cards, and open/closed filter states.
- Watchlist and Favorites tab text colors.
- Spotlight and pause-screen action buttons.
- Music/remote player controls.
- Sidebar labels created by Enhanced companion pages.

If a newly enabled Enhanced feature looks unstyled, it may use a selector Spookyfin has not seen yet. Keep the feature enabled, take a screenshot, and update the theme rules for that screen.

## Helpful Links

- [Jellyfin Enhanced](https://github.com/n00bcodr/Jellyfin-Enhanced)
- [Jellyfin Enhanced installation guide](https://n00bcodr.github.io/Jellyfin-Enhanced/installation/installation/)
- [Jellyfin Enhanced feature overview](https://n00bcodr.github.io/Jellyfin-Enhanced/enhanced/enhanced-features/)
- [Jellyfin Enhanced *arr features](https://n00bcodr.github.io/Jellyfin-Enhanced/arr/arr-features/)
- [File Transformation plugin](https://github.com/IAmParadox27/jellyfin-plugin-file-transformation)
