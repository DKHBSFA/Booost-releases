# Booost — Downloads & Auto-Update Feed

**Booost is LinkedIn growth software that runs on your own computer, not in someone
else's cloud.** Multi-step outreach campaigns, AI-written comments and posts in your
own voice, contact intelligence, and an anti-ban system that paces every action and
stops the moment something looks wrong. **Your LinkedIn session never leaves your
machine** — Booost never receives your LinkedIn password — and your profiles, messages
and campaigns live in a SQLite file on your own disk.

| | |
|---|---|
| 🌐 Website | **https://booost.network** |
| 📖 Blog | https://booost.network/blog/ — what actually triggers a LinkedIn restriction, and what it costs when it happens |
| 🗺️ Roadmap | https://booost.network/roadmap/ — what is built, and what isn't |
| ⚖️ Legal & privacy | https://booost.network/legal/ |
| 💬 Contact | https://booost.network/contact/ |
| 🚀 Launch | **1 September 2026.** The waitlist is open at https://booost.network |

This repository hosts the **installers** for the Booost desktop app and the
**auto-update feed** the app reads (via electron-updater). The application source code
lives in a separate, private repository. Made by [Alfercom Srl](https://booost.network/about/), Padua, Italy.

> 👉 **Most people just want the [latest release](../../releases/latest).** Open it
> and pick the one file for your system from the table below.

## Which file do I download?

### 🖥️ Desktop app — Booost Business

| Your system | Download this file | How to install |
|---|---|---|
| **Windows** | `Booost-Setup-<version>.exe` | Double-click and follow the installer. |
| **macOS — Apple Silicon** (M1/M2/M3/M4) | `Booost-<version>-arm64.dmg` | Open the `.dmg`, drag **Booost** into Applications. |
| **Linux — most distros** | `Booost-<version>.AppImage` | `chmod +x Booost-<version>.AppImage`, then run it. |
| **Linux — Debian/Ubuntu** | `booost_<version>_amd64.deb` | `sudo dpkg -i booost_<version>_amd64.deb` |

> **Which Mac do I have?** Apple menu → *About This Mac*. If it says "Apple M…",
> it's Apple Silicon. (Intel Macs aren't currently provided — ask us if you need one.)

### 🧩 Browser extension — Booost Personal

**Not published yet.** Booost Personal ships with the launch on **1 September 2026**,
through the Chrome and Firefox stores.

⚠️ A `booost-extension-<version>.zip` is attached to earlier releases by the build
pipeline. It is a **build artifact, not the product** — don't install it.

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

## Two editions

Both Booost Business (desktop) and Booost Personal (extension) ship in two editions:
**Pro** includes Booost's managed AI and every workflow module; **Basic** is the same
product driven by your own AI provider key — 20 providers, Ollama included — and costs
less. Prices and the founding offer are on [booost.network](https://booost.network).

## Found a bug, or something unclear?

Open an issue here, or write to us from [booost.network/contact](https://booost.network/contact/).
