# Third-party notices

Horizon's own source code is licensed under the [MIT License](LICENSE). The binary distribution
(the installer and the installed program) also contains the following third-party components, each
under its own license.

| Component | Used for | License | Source |
|---|---|---|---|
| .NET runtime, WPF, Windows Forms | Application runtime (shipped self-contained) | MIT | https://github.com/dotnet |
| WPF UI (lepoco) | Fluent controls and theme of the dashboard | MIT | https://github.com/lepoco/wpfui |
| Fluent System Icons (via WPF UI) | Icons | MIT | https://github.com/microsoft/fluentui-system-icons |
| LibVLCSharp | .NET binding to libVLC | LGPL-2.1-or-later | https://code.videolan.org/videolan/LibVLCSharp |
| libVLC 3.0.x and its plugins (VideoLAN.LibVLC.Windows) | Video decoding and presentation | LGPL-2.1-or-later; some plugins GPL-2.0-or-later | https://code.videolan.org/videolan/vlc |
| FFmpeg / libavcodec (inside libVLC) | Video decoders | LGPL-2.1-or-later / GPL-2.0-or-later (as built by VideoLAN) | https://ffmpeg.org |
| NAudio (NAudio.Wasapi, NAudio.Core) | System-audio levels for audio-reactive wallpapers | MIT | https://github.com/naudio/NAudio |
| Microsoft.Web.WebView2 (SDK) | Hosting web wallpapers | BSD-3-Clause-style (Microsoft) | https://www.nuget.org/packages/Microsoft.Web.WebView2 |
| Windows App SDK / WinUI 3 (installer only) | Installer and uninstaller UI | MIT | https://github.com/microsoft/WindowsAppSDK |

Not shipped, used from Windows: the Microsoft Edge WebView2 Runtime (part of Windows 11).

## Notes on LGPL/GPL components (libVLC, FFmpeg)

- libVLC is loaded dynamically from `libvlc\win-x64` next to `Horizon.exe` and is not modified. You
  may replace those files with a compatible build of your own (LGPL §6).
- Some VLC plugins are licensed under GPL-2.0-or-later. Horizon's MIT license is GPL-compatible, so
  distributing them together is permitted. Whoever distributes Horizon binaries must make the
  corresponding source code of these components available, for example by linking to the exact
  VideoLAN source release (`vlc-3.0.21`, https://download.videolan.org/pub/videolan/vlc/3.0.21/) and
  including their license texts (`COPYING`, `COPYING.LIB`).
- The published build removes libVLC plugins that Horizon never uses (stream output, muxers,
  visualizations, Lua, network access, …).

The full license texts of these components are available at the source links above and inside their
NuGet packages.
