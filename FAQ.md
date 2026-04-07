# Fusion FAQ

This FAQ is meant to complement the starter guide. It focuses on common Fusion questions and app behavior that are not already covered in the main setup walkthrough.

## General

### What is Fusion?

Fusion is a media companion app for Apple platforms. It helps you discover, organize, and track movies and TV shows from one interface, with support for customizable home layouts, metadata, watch history, collections, and optional third-party extensions.

### Which devices does Fusion support?

Fusion supports iPhone, iPad, Mac, and Apple TV. Support is currently limited to iOS/iPadOS, macOS, and tvOS 26+.

### Does Fusion include or host any content?

No. Fusion does not provide, host, stream, or distribute media content. It is a media browser and organizer. Any extensions or content sources are added by the user, and Fusion assumes those sources are legal and user-controlled.

### Are addons built into Fusion?

No. Addons are user-configured URLs that you add yourself in `Settings > Addons`. Fusion does not bundle or control what those endpoints provide.

## Progress and Tracking

### Should I use Local, Trakt, or AniList progress?

Use `Local` if you want device-only progress with no external account. Use `Trakt` if you already track most of your watching there. Use `AniList` if anime is your main focus and you want anime-first tracking.

### How do I connect Trakt?

Open `Settings > Accounts > Trakt` and choose `Connect to Trakt`.

- On iPhone and Mac, Fusion opens a browser so you can sign in and approve access.
- On Apple TV, Fusion gives you a code and verification URL to finish on another device.

Once connected, the Trakt status should show as connected and the Trakt sync options under `Settings > Progress > Trakt` should become available.

### Why is Continue Watching not updating?

Check these first:

1. Confirm your storage mode in `Settings > Progress`.
2. If you use Trakt, make sure your Trakt account is connected.
3. In `Settings > Progress > Trakt`, turn on `Scrobble Playback` and run `Sync Now`.
4. If you use external players, enable `Sync After External Playback`.
5. If it is still wrong, switch to `Local`, test one playback, then switch back and sync again.

### How can I tell whether progress was actually saved?

Play something briefly, exit playback normally, then check `Home > Continue Watching`. If you use Trakt, also open `Settings > Progress > Trakt`, run `Sync Now`, and confirm the last sync time updates.

### What does Source Switcher do?

Source Switcher changes which progress sources feed Continue Watching and related views. Common setups include `All Local`, `All Trakt`, `Trakt + AniList`, or `Anime Local + AniList`. It also gives quick access to sync and cache-clear actions.

### Where does the watchlist button save items?

That depends on the provider you choose in `Settings > Progress`. Fusion can use Trakt or PublicMetaDB for the watchlist button. If Trakt is connected, it is the default association. One useful limitation to know: Trakt watchlists have a 100-item cap.

## Metadata and Anime

### Which metadata source should I use?

The best default depends on the type of media:

- Movies: TMDB is usually the best primary source.
- Series: TMDB or TVDB both work well, depending on which structure you prefer.
- Anime: TVDB is the safest default for episode and season structure.

If you want more control, Fusion also lets you set field-specific overrides for things like hero images, episode backgrounds, synopsis, and structure.

### Why does Fusion warn me when I change anime metadata or structure sources?

Because anime numbering can differ between providers. Changing the structure or image source away from the recommended setup can break episode mapping, make season ordering look wrong, or cause watch-status sync to appear incorrect.

### Where do anime watched checkmarks come from?

You can choose the source in `Settings > Progress > Anime Tracking > Show Watched From`. The options are `Local`, `Trakt`, `AniList`, or `All Sources`. If you watch across multiple devices or apps, `All Sources` is usually the safest choice.

## Home Screen and Customization

### What are collections in Fusion?

Collections are custom folders on your Home screen. Each collection tile can have its own title, image, tile shape, and one or more content sources. When opened, Fusion shows a grid built from those sources.

### What happens if a collection has multiple sources?

If a collection has one source, Fusion opens that source directly. If it has two or more, Fusion merges them into a single combined grid. If it has no sources, the collection will show as not configured.

### Can I disable a widget without deleting it?

No. Fusion does not currently have a true disable toggle for widgets. If you want to hide one, you need to delete it and add or import it again later.

### What settings do people commonly miss after first setup?

The most commonly overlooked ones are:

- `Progress Storage` and whether it should be Local or Trakt
- `Watchlist Button` provider
- `Video Player` and per-media-type player selection
- `Autoplay Next Episode`
- `Remember Last Source`
- `Up Next` timing
- Subtitle presets, size, colors, and position
- Addon timeout settings
- iCloud sync
- Continue Watching sync and push/pull options

## Playback

### How do I customize subtitles?

Go to `Settings > Subtitles`. From there, you can use built-in presets or adjust subtitle size, position, and colors manually.

### Will HDR video look washed out on an SDR Apple TV setup?

No. Fusion relies on Apple's system-level tone mapping on tvOS. If you play HDR content on an SDR display, Apple TV handles the tone mapping rather than leaving the image washed out.
