# Clip & Board

**Your clipboard, remembered.**

Clip & Board is a native macOS clipboard manager. It keeps the text and links you copy, lets you search them, and puts them back on your clipboard. Your history is encrypted and stored on your Mac.

**[Download the latest version](https://github.com/devtownhall/clip-and-board/releases/latest/download/Clip-and-Board.zip)** · [devtownhall.com/clipboard](https://devtownhall.com/clipboard)

Requires **macOS 14 or later** on a Mac with **Apple Silicon**.

This repository publishes releases only. The source code isn't public.

## Install

1. Download `Clip-and-Board.zip` from the [latest release](https://github.com/devtownhall/clip-and-board/releases/latest) and open it.
2. Move **Clip & Board** to your Applications folder and open it. It lives in the menu bar and has no Dock icon.
3. On macOS 15.4 and later, macOS asks before an app can read what you copy in other apps. Choose **Always Allow**. If you miss the prompt, set it in **System Settings → Privacy & Security**.

Press **⌃⌘V** in any app to open your history. You can change the shortcut in Settings.

## Using it

| Key | Action |
|---|---|
| ⌃⌘V | Open Clip & Board from any app |
| type | Search. Case and accents are ignored, and every word has to match |
| ↑ / ↓ | Move through history |
| ↩ | Put the selected item back on the clipboard |
| ⌘S | Favorite. Favorites are kept regardless of retention and item limits |
| ⌫ | Delete. ⌘Z undoes it for 5 seconds |
| esc | Close |

Choosing an item puts it back on your clipboard, ready for ⌘V. To have Clip & Board press ⌘V for you, turn on **Settings → General → Paste automatically** and allow Accessibility access.

You can also click the notch, or the top centre of the menu bar on screens without one, to see your last 6 copies.

Clip & Board stores text and links. It doesn't store images or files.

## Privacy

- **Stored on your Mac, encrypted.** History is encrypted with AES-256-GCM. The key is kept in your macOS Keychain.
- **No internet code.** No servers, cloud, uploads or update checks. No account, analytics, telemetry or AI processing.
- **Secrets are caught on your Mac.** Recognised API keys and private keys are never stored. Tokens such as JWTs and one-time codes are deleted after 30 seconds. Detection is heuristic, so it can't catch every secret.
- **Password managers are respected.** Items they mark as concealed or transient are never recorded.
- **Sync is optional, and off by default.** If you turn it on, new copies go straight to your own paired Macs on the same network, end-to-end encrypted, with no server in between.

## Updates

Clip & Board never checks for updates, because it has no internet code. To hear about new versions, choose **Watch → Custom → Releases** on this repository.

To update, quit Clip & Board from the menu bar, replace the app in Applications, and open it again. Your history stays.

## Checking a download

Each release lists the SHA-256 of its zip. To compare:

```sh
shasum -a 256 ~/Downloads/Clip-and-Board.zip
```

## Removing it

1. Optionally, clear your history in **Settings → History → Clear All History…**, and unpair your Macs in **Settings → Sync**.
2. Quit Clip & Board from the menu bar and move it to the Trash.
3. To remove everything, also delete these. The app was previously called ClipVault, and these kept that name:
   - The folder `~/Library/Application Support/ClipVault/`.
   - In Keychain Access, the items whose **Where** is `com.devtownhall.clipvault` or starts with `com.devtownhall.clipvault.sync`.

## Contact

Questions or problems: [devtownhall.com/#contact](https://devtownhall.com/#contact)

© 2026 DevTownHall
