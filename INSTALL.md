# Install Gotland World

Download the files for your platform from the [download release](https://github.com/mannetroll/gotlandgame/releases/latest). Both platforms are v0.1.3 with compact terrain storage. Both are built from macOS.23 (`5cf0342a7`). Keep all parts in one folder and retain their exact names. Allow at least 18 GB free while downloading and installing. The installed macOS app uses approximately 5.47 GB; Windows uses approximately 5.52 GB.

## macOS — Apple Silicon

Requires macOS 12 or later on an Apple Silicon Mac. Intel Macs are not supported by this download.

1. Download `GotlandWorld-v0.1.3-macOS-arm64.dmg` and both accompanying parts (`.002.dmgpart`, `.003.dmgpart`) into the same folder.
2. Open the `.dmg` file. macOS reads the accompanying parts automatically.
3. Drag `GotlandWorld.app` to Applications. Keep the accompanying licence notices if you redistribute the game.
4. Eject the disk image, then open GotlandWorld from Applications.

The application has a verified ad-hoc signature but is not Developer ID signed or Apple-notarized. macOS may block its first launch. After checking the download and deciding to trust it, use **System Settings → Privacy & Security → Open Anyway** following the blocked attempt. See [Apple's instructions](https://support.apple.com/en-us/102445). Keep normal system security enabled. If macOS reports malware rather than an unidentified developer, do not override that warning.

If the disk image cannot open, confirm all three files finished downloading, are in the same folder and have not acquired suffixes such as `(1)`. Compare their checksums before downloading again.

## Windows 10 and Windows 11 — x64

Requires Windows 10 22H2 (build 19045) or later, including Windows 11, and a Direct3D 11 capable GPU. The same installer runs on both operating systems.

1. Download `GotlandWorld-v0.1.3-Windows-x64-Setup.exe` and all three matching data parts, `GotlandWorld-v0.1.3-Windows-x64-Setup-1.bin` through `GotlandWorld-v0.1.3-Windows-x64-Setup-3.bin` from the release into the same folder.
2. Open the Setup executable and choose the install folder. Installation is per-user and does not require administrator rights.
3. Launch **Gotland World** from the Start menu or the optional Desktop shortcut.

The installer, launcher, Desktop shortcut and Start menu shortcut use the Kovik chapel icon. Upgrades replace the managed player files; game settings are stored separately. When replacing an earlier v0.1.3 download, download the complete new set of installer files and do not mix old and new parts.

The installer and game executable are not publisher-signed, so Windows may display a reputation warning. Verify the download before deciding whether to run it. The installer includes the game and its runtime; no Unity Editor or separate .NET installation is required.

The portable game layout remains `GotlandWorld.exe` beside `GotlandWorld_Data`. Keep those two entries together if moving the installed game. The installer also adds documentation and an uninstaller. Uninstall through Windows **Settings → Apps → Installed apps**.

## Verify downloads

Download [`SHA256SUMS`](https://github.com/mannetroll/gotlandgame/releases/download/v0.1.3/SHA256SUMS) into the folder containing your platform’s files.

On macOS, open Terminal in that folder and run:

```sh
grep 'macOS-arm64' SHA256SUMS | shasum -a 256 -c -
```

On Windows, open PowerShell in the download folder and run:

```powershell
Get-Content .\SHA256SUMS | Where-Object { $_ -match 'Windows-x64' } | ForEach-Object {
    $expected, $file = $_ -split '  ', 2
    if ((Get-FileHash -Algorithm SHA256 -LiteralPath $file).Hash.ToLowerInvariant() -ne $expected) {
        throw "Checksum mismatch: $file"
    }
    Write-Host "OK: $file"
}
```

Every file for the selected platform must report OK. Keep the parts until installation finishes; the installed game no longer needs the downloaded installer or disk-image parts.
