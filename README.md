<p align="center">
  <img src="docs/icon.png" width="112" alt="Horizon icon">
</p>

<h1 align="center">Horizon</h1>

<p align="center">
  <b>Live wallpapers for Windows: videos, images and web pages behind your desktop icons.</b><br>
  GPU-accelerated, multi-monitor, and practically invisible to your system.
</p>

<p align="center">
  <a href="https://github.com/plysystems/Horizon-Releases/releases/latest"><img alt="Latest release" src="https://img.shields.io/github/v/release/plysystems/Horizon-Releases?label=download&style=flat-square"></a>
  <img alt="Windows 10/11 x64" src="https://img.shields.io/badge/Windows-10%20%7C%2011%20x64-0078D4?style=flat-square">
  <a href="LICENSE"><img alt="MIT License" src="https://img.shields.io/badge/license-MIT-green?style=flat-square"></a>
</p>

This repository is Horizon's **official download and update channel**. Installed copies of Horizon
check it for new versions.

## Download

**[⬇ Download the latest HorizonSetup.exe](https://github.com/plysystems/Horizon-Releases/releases/latest)**

Run it, that's all: one file, **no .NET, no admin rights, no restart**. Horizon installs for your
account into `%LocalAppData%\Programs\Horizon`. Requirements: Windows 10 (1809+) or 11, 64-bit.

> The installer isn't code-signed yet, so Windows SmartScreen may show "Windows protected your PC".
> Choose **More info → Run anyway**.

**Verify your download (optional):** every release lists the SHA-256 in `HorizonSetup-<version>.exe.sha256`.

```powershell
Get-FileHash .\HorizonSetup-1.0.1.exe -Algorithm SHA256
```

## Features

- 🎬 Videos, images, web pages and WebGL shaders as wallpaper
- 🖥️ Multi-monitor: same everywhere, per display, or one picture spanned across all screens;
  Fill / Fit / Stretch / Tile / Center
- 🖼️ Gallery with hover preview and one-click apply; day/night wallpapers with crossfades; playlists
- ⚡ GPU decoding, 30/60 FPS cap, auto-pause when a display is covered, on battery or while locked;
  about 12 MB RAM and ~0 % CPU in the tray
- 💤 Screensaver mode · 🖱️ double-click the desktop to hide icons · 🔊 audio-reactive web wallpapers
- 🔄 Updates itself from this channel (version + build hash, SHA-256 verified)
- 🌍 English and German · light and dark mode

## Updates

Horizon reads `update.json` from the latest release here, two minutes after start and then once a
day (can be turned off under *Updates*). It contains the version, the **build hash** (the source
commit the release was built from) and the setup's SHA-256. A newer version, or a rebuilt release
with a different build hash, is offered as an update. The download is verified against the checksum
before it's installed silently; your settings, library, autostart and shortcuts are kept. No account,
no telemetry: it's a plain HTTPS download.

## Uninstall

**Settings → Apps → Installed apps → Horizon → Uninstall**. Your static wallpaper, desktop icons and
previous screensaver are restored. Optionally your settings and library list are deleted too; your
media files are never touched.

---

### Deutsch

Hier gibt es die offiziellen Downloads von **Horizon**: Videos, Bilder und Webseiten als
Desktop-Hintergrund, GPU-beschleunigt und für das System nahezu unsichtbar.
**[Neueste HorizonSetup.exe herunterladen](https://github.com/plysystems/Horizon-Releases/releases/latest)**,
starten, fertig. Keine Adminrechte, kein .NET nötig. Horizon aktualisiert sich über diesen Kanal
selbst; jedes Update wird vor der Installation per SHA-256 geprüft.

## License

Horizon is licensed under the [MIT License](LICENSE). The download includes third-party components
under their own licenses (notably libVLC, LGPL-2.1+, with some GPL plugins); see
[THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md).
