# Booost — Downloads & Auto-Update Feed

This repository hosts the **installers** for the Booost desktop app and the
**auto-update feed** the app reads (via electron-updater). The application source
code lives in a separate, private repository.

> 👉 **Most people just want the [latest release](../../releases/latest).** Open it
> and pick the one file for your system from the table below.

## Which file do I download?

### 🖥️ Desktop app

| Your system | Download this file | How to install |
|---|---|---|
| **Windows** | `Booost-Setup-<version>.exe` | Double-click and follow the installer. |
| **macOS — Apple Silicon** (M1/M2/M3/M4) | `Booost-<version>-arm64.dmg` | Open the `.dmg`, drag **Booost** into Applications. |
| **Linux — most distros** | `Booost-<version>.AppImage` | `chmod +x Booost-<version>.AppImage`, then run it. |
| **Linux — Debian/Ubuntu** | `booost_<version>_amd64.deb` | `sudo dpkg -i booost_<version>_amd64.deb` |

> **Which Mac do I have?** Apple menu → *About This Mac*. If it says "Apple M…",
> it's Apple Silicon. (Intel Macs aren't currently provided — ask us if you need one.)

### 🧩 Browser extension

| File | What it is |
|---|---|
| `booost-extension-<version>.zip` | The companion browser extension (Chrome / Edge / Chromium). Unzip it, then in your browser open the extensions page → enable **Developer mode** → **Load unpacked** → select the unzipped folder. |

### ⚙️ Files you can ignore

These are used **automatically** by the in-app updater — you never download them by hand:

- `latest.yml`, `latest-mac.yml`, `latest-linux.yml` — update manifests the app checks
- `*.blockmap` — delta-update data (smaller updates)
- `Booost-<version>-arm64-mac.zip` — the macOS package the auto-updater uses
- `builder-debug.yml` — build metadata

## Auto-updates

Once installed, Booost checks this repository on launch and updates itself
automatically. You normally only come here for the **first** install.

## macOS: "Booost can't be opened because Apple cannot check it"

The macOS builds aren't code-signed yet, so Gatekeeper warns on first open. Either:

- Right-click (or Control-click) **Booost** → **Open** → **Open**, or
- run `xattr -dr com.apple.quarantine /Applications/Booost.app` in Terminal once.
