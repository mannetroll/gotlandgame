# Gotland World

**Take the coastal road. Look around. Stop wherever curiosity takes you.**

Drive and explore Gotland and Fårö, visit Visby and coastal landmarks, or let autopilot take you on a tour. Gotland Ring is included for circuit driving.

**[Watch the coastal trailer](https://mannetroll.github.io/gotlandgame/)** · **[Download v0.1.0](https://github.com/mannetroll/gotlandgame/releases/tag/v0.1.0)** · **[Installation guide](INSTALL.md)**

This public repository contains player documentation, screenshots, a trailer and credits. The compiled games are attached to Releases. No game source code, Unity project or development history is included.

![Driving beside Visby's city wall](images/visby.png)

## Trailer

[Watch the 39-second coastal trailer](https://mannetroll.github.io/gotlandgame/) with sound, directly in your browser on iPhone or desktop. This is actual footage from the macOS development preview, showing daylight, moving vegetation and the living soundscape. These improvements are newer than the current v0.1.0 public release.

## Downloads

Download **every file for your platform** into the same folder and keep their names unchanged. The complete world is around 4.3 GB installed. GitHub's per-file limit requires multiple parts; the disk image or installer reads them together.

| Platform | Download | Open after downloading all parts |
|---|---|---|
| macOS 12 or later, Apple Silicon | [Disk image](https://github.com/mannetroll/gotlandgame/releases/download/v0.1.0/GotlandWorld-v0.1.0-macOS-arm64.dmg) · [Part 2](https://github.com/mannetroll/gotlandgame/releases/download/v0.1.0/GotlandWorld-v0.1.0-macOS-arm64.002.dmgpart) | The `.dmg` file |
| Windows 11, x64 | [Setup](https://github.com/mannetroll/gotlandgame/releases/download/v0.1.0/GotlandWorld-v0.1.0-Windows-x64-Setup.exe) · [Data 1](https://github.com/mannetroll/gotlandgame/releases/download/v0.1.0/GotlandWorld-v0.1.0-Windows-x64-Setup-1.bin) · [Data 2](https://github.com/mannetroll/gotlandgame/releases/download/v0.1.0/GotlandWorld-v0.1.0-Windows-x64-Setup-2.bin) | The `Setup.exe` file |

[SHA-256 checksums](https://github.com/mannetroll/gotlandgame/releases/download/v0.1.0/SHA256SUMS) are available for all downloads. See [installation instructions](INSTALL.md) for verification and first-launch details. No Unity Editor, .NET installation, account or geographic downloads are required to play.

Use the named game files under **Releases → Assets**. GitHub's automatic **Source code (zip/tar.gz)** links contain only this documentation repository; they are not game downloads.

## Play

Touring starts near Fiskarporten in Visby. Explore roads and landmarks, use the G map to search destinations and warp, or choose an autopilot route. Open Escape to switch to Gotland Ring.

| Key | Action |
|---|---|
| W / Up · S / Down | Accelerate · brake |
| A / D or Left / Right | Steer |
| X | Brake into reverse; release the accelerator first |
| Mouse · right-click | Look around · centre view |
| U | Toggle mouse steering |
| P | Join the nearest autopilot-route point and drive |
| R | Recover to the nearest drivable road |
| G | Open or close the touring map |
| + | Jump one kilometre along the route |
| C | Cycle cockpit, bonnet, follow and drone cameras |
| Y · T | Change car · paint where supported |
| H | Switch AWD / Arcade handling |
| B · E | Find a petrol station · refuel when stopped at a pump |
| M · F | Toggle sound · fullscreen |
| Escape | Pause, settings and driving mode |

On Gotland Ring, autopilot uses Cmd+P on Mac or Ctrl+P on Windows; fullscreen uses Cmd+F / Ctrl+F. F3 opens driving settings, Z switches to the training area and Home restarts the lap (Fn+Left on compact Mac keyboards).

![Kovik Chapel in the game](images/kovik.png)

This is a prototype. Buildings and scenery combine mapped geometry, measurements and estimated details. Autopilot is experimental and can drive very fast. Some offshore terrain is provisional. The game is not a navigation or road-safety tool.

## Credits and use

This is an unofficial fan-made prototype, not affiliated with or endorsed by GotlandRing, Subaru Corporation or their affiliates.

The included car models use **CC BY-NC 4.0**. Builds containing them are for **noncommercial use**. Keep the licence and attribution files with redistributed copies. The original software's MIT licence does not replace separate asset, data or Unity runtime terms.

- [Third-party notices and data credits](THIRD_PARTY_NOTICES.md)
- [Original software licence](LICENSE)
- [Microsoft building-data licence](LICENSE-CDLA-Permissive-2.0.txt)

Release v0.1.0 packages the existing macOS.15 game builds. The inherited internal player version may display v0.3.3; the public download release is v0.1.0.
