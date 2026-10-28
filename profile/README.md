<div align="center">

<img src="./assets/sonara-logo.jpg" alt="Sonara logo" width="220" />

### Music sources for Lavalink.

[**Sonara**](https://github.com/SonaraHQ/Sonara) · [**Sonara-API**](https://github.com/SonaraHQ/Sonara-API) · [**Lavalink**](https://lavalink.dev/)

</div>

---

### About

Sonara is a Lavalink plugin that loads tracks from many music services (Spotify, Apple Music, Deezer, Tidal, SoundCloud and more) and plays them directly or through your own mirror providers, such as YouTube.

It is a fork of [PulseLink](https://github.com/ItzRandom23/PulseLink), which is based on [LavaSrc](https://github.com/topi314/LavaSrc). Sonara adds fixes and features on top, and runs its Spotify support on infrastructure you host yourself instead of a third-party server.

### Repositories

| Repository | What it is |
|---|---|
| [**Sonara**](https://github.com/SonaraHQ/Sonara) | The Lavalink plugin (Java). Audio sources, mirroring, LavaSearch and LavaLyrics support. |
| [**Sonara-API**](https://github.com/SonaraHQ/Sonara-API) | A self-hosted Spotify resolver (Node.js). Loads playlists and recommendations through Spotify's web player API, including Spotify-made playlists such as Daily Mix and Top 50, and serves an anonymous Spotify token. |

### What Sonara adds

- **Spotify without a third-party server:** tracks, albums, artists and search use the official Spotify Web API, and playlists and recommendations use your own Sonara-API.
- **Spotify-made playlists:** Daily Mix, Discover Weekly, Top 50 and radios load through Sonara-API, even though the public Web API blocks them.
- **More reliable lyrics:** LRCLIB lyrics no longer fail on lines without a space after the timestamp, and one failing lyrics source no longer breaks the whole lyrics lookup.
- **Safer credentials:** logins in configured URLs are sent as headers and never show up in logs.

### Getting started

Add Sonara to your Lavalink `application.yml`:

```yaml
lavalink:
  plugins:
    - dependency: "com.github.SonaraHQ:Sonara:1.0.0"
      repository: "https://jitpack.io"
```

Then configure it under `plugins.sonara`. See the [Sonara README](https://github.com/SonaraHQ/Sonara#readme) and [`application.example.yml`](https://github.com/SonaraHQ/Sonara/blob/main/application.example.yml) for every option, and the [Sonara-API README](https://github.com/SonaraHQ/Sonara-API#readme) to host your own Spotify resolver.

### Credits

Sonara builds on the work of others:

- [PulseLink](https://github.com/ItzRandom23/PulseLink) by ItzRandom23, the project Sonara is forked from (Apache 2.0)
- [LavaSrc](https://github.com/topi314/LavaSrc) and [LavaLyrics](https://github.com/topi314/LavaLyrics) by topi314 and contributors
- [anonify](https://github.com/devoxin/anonify) by devoxin, which Sonara-API's token server is based on
- [Lavalink](https://github.com/lavalink-devs/Lavalink) and [Lavaplayer](https://github.com/lavalink-devs/lavaplayer)

---

<div align="center">
  <sub>Built for the Lavalink ecosystem.</sub>
</div>
