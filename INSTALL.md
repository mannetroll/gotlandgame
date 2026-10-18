# Install Gotland World

Download the files for your platform from [release v0.1.1](https://github.com/mannetroll/gotlandgame/releases/tag/v0.1.1). Keep all parts in one folder and retain their exact names. Allow at least 12 GB free while downloading and installing. The installed game needs around 4.7 GB.

## macOS — Apple Silicon

Requires macOS 12 or later on an Apple Silicon Mac. Intel Macs are not supported by this download.

1. Download `GotlandWorld-v0.1.1-macOS-arm64.dmg` and `GotlandWorld-v0.1.1-macOS-arm64.002.dmgpart` into the same folder.
2. Open the `.dmg` file. macOS reads the accompanying part automatically.
3. Drag `GotlandWorld.app` to Applications. Keep the accompanying licence notices if you redistribute the game.
4. Eject the disk image, then open GotlandWorld from Applications.

The application has a verified ad-hoc signature but is not Developer ID signed or Apple-notarized. macOS may block its first launch. After checking the download and deciding to trust it, use **System Settings → Privacy & Security → Open Anyway** following the blocked attempt. See [Apple's instructions](https://support.apple.com/en-us/102445). Keep normal system security enabled. If macOS reports malware rather than an unidentified developer, do not override that warning.

If the disk image cannot open, confirm both files finished downloading, are in the same folder and have not acquired suffixes such as `(1)`. Compare their checksums before downloading again.

## Windows 11 — x64

1. Download `GotlandWorld-v0.1.1-Windows-x64-Setup.exe`, `GotlandWorld-v0.1.1-Windows-x64-Setup-1.bin` and `GotlandWorld-v0.1.1-Windows-x64-Setup-2.bin` into the same folder.
2. Open the Setup executable and choose the install folder. Installation is per-user and does not require administrator rights.
3. Launch **Gotland World** from the Start menu or the optional Desktop shortcut.

The installer, launcher, Desktop shortcut and Start menu shortcut use the Kovik chapel icon.

The installer and game executable are not publisher-signed, so Windows may display a reputation warning. Verify the download before deciding whether to run it. The installer includes the game and its runtime; no Unity Editor or separate .NET installation is required.

The portable game layout remains `GotlandWorld.exe` beside `GotlandWorld_Data`. Keep those two entries together if moving the installed game. The installer also adds documentation and an uninstaller. Uninstall through Windows **Settings → Apps → Installed apps**.

## Verify downloads

Download `SHA256SUMS` into the folder containing your platform's files.

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
