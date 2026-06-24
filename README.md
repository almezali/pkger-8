<div align="center">

<br/>

```
██████╗ ██╗  ██╗ ██████╗ ███████╗██████╗
██╔══██╗██║ ██╔╝██╔════╝ ██╔════╝██╔══██╗
██████╔╝█████╔╝ ██║  ███╗█████╗  ██████╔╝
██╔═══╝ ██╔═██╗ ██║   ██║██╔══╝  ██╔══██╗
██║     ██║  ██╗╚██████╔╝███████╗██║  ██║
╚═╝     ╚═╝  ╚═╝ ╚═════╝ ╚══════╝╚═╝  ╚═╝
```

**A modern, native GTK 4 package manager for Fedora Linux and its derivatives**

[![Version-1.0.1](https://img.shields.io/badge/version-1.0.1-blue?style=for-the-badge&logo=linux)](https://github.com/almezali/pkger-8/releases/tag/1.0.1)
[![Version-1.0.2](https://img.shields.io/badge/version-1.0.2-red?style=for-the-badge&logo=linux)]
(https://github.com/almezali/pkger-8/releases/tag/1.0.2)
[![GTK](https://img.shields.io/badge/GTK-4.0-green?style=for-the-badge&logo=gnome)](https://gtk.org)
[![Python](https://img.shields.io/badge/Python-3.13+-yellow?style=for-the-badge&logo=python)](https://python.org)
[![Fedora](https://img.shields.io/badge/Fedora-Linux-294172?style=for-the-badge&logo=fedora)](https://fedoraproject.org)

<br/>

[**Download RPM**](https://github.com/almezali/pkger-8/releases/download/1.0.1/pkger-1.0.1-1.x86_64.rpm) • [**Download AppImage**](https://github.com/almezali/pkger-8/releases/download/1.0.1/Pkger-x86_64.AppImage) • [**Screenshots**](#-screenshots) • [**Features**](#-features)

</div>

---

## Overview

**PKGER** is a powerful, fully native desktop package manager built with **GTK 4** and **Python 3.13+**, designed specifically for **Fedora Linux** and its derivatives. It provides a clean, modern interface to manage RPM packages, Flatpaks, AppImages, and system repositories — all from a single window.


---

## 📸 Screenshots

<div align="center">

| Install Workspace | Updates Manager |
|:-:|:-:|
| ![Install](https://github.com/almezali/pkger-8/blob/main/Screenshot/Screenshot_01.png) | ![Updates](https://github.com/almezali/pkger-8/blob/main/Screenshot/Screenshot_02.png) |

| Repository Manager | System Tools |
|:-:|:-:|
| ![Repos](https://github.com/almezali/pkger-8/blob/main/Screenshot/Screenshot_03.png) | ![System](https://github.com/almezali/pkger-8/blob/main/Screenshot/Screenshot_04.png) |

</div>

---

## ✨ Features

### 📦 Package Management
- **Unified search** across official Fedora repos, COPR, installed packages, Flatpak, and AppImages simultaneously
- **Multi-source install modes** — Official, COPR, Installed (native / foreign / Flatpak / AppImage), Flatpak, Developer/packager search
- **Smart fuzzy matching** with semantic category hints (browser, music, video, games, KDE, GNOME, etc.)
- **Client-side filtering** and real-time sorting by name, version, repository, install status, or description
- **Local RPM install** — pick any `.rpm` file from disk and install it directly
- **Batch operations** — add multiple packages to a batch list and install/remove them in one shot
- **Export visible results** to a plain-text file for offline reference or scripting
- **Threaded background search** with generation tokens — stale results are silently discarded, the UI never blocks

### 🔄 Updates Center
- Unified **DNF + Flatpak** pending update detection in a single view
- **Security advisory enrichment** — each RPM update shows its advisory ID, severity (Critical / Important / Moderate / Low), and type
- **Estimated download size** for all pending RPM upgrades
- **Selective upgrade** — check individual packages, click "Security" to auto-select all security-related updates, then apply only what you choose
- **Sync & Refresh** to pull fresh repository metadata before scanning
- **Version diff view** — see exactly what version is installed and what is available

### 🗂️ Repository Manager
- Full list of configured DNF repositories with kind classification (Fedora official, RPM Fusion, COPR, Third-party)
- **Enable / Disable** repositories with a single click (no terminal required)
- **Add repositories** via:
  - 🔖 **Presets** — RPM Fusion Free, Nonfree, or both at once
  - 🌐 **URL** — paste any `.repo` file HTTPS URL
  - 📁 **Local file** — pick a `.repo` file from disk
  - 🧪 **COPR** — enable any Copr project by `owner/project`
  - ⚙️ **Manual** — full custom entry with baseurl, GPG key, and toggle options
- **Per-repo package search** — search packages inside any selected repository
- **Batch install/remove** from repository package results
- **Export search results** to tab-separated text

### 🖼️ AppImage Manager
- **Recursive home-directory scan** for `.AppImage` files (smart skip for `.cache`, `.npm`, `.cargo`, `.git`, and similar heavy directories)
- **Import AppImage** — copy any AppImage to `~/Applications` and mark it executable automatically
- **Launch selected** AppImage directly from the UI
- **Remove** AppImage files safely with confirmation dialog
- Live filter by name or path

### 🛠️ System Tools
- **One-click maintenance actions**: full upgrade, metadata refresh, cache clean, deep clean, orphan removal, dependency fix, dracut initramfs rebuild, GRUB config regeneration
- **System diagnostics** built-in: `dnf check-update`, foreign packages, explicitly installed packages, `systemctl --failed`, journal errors, disk usage, memory, repo list, DNF history
- **Flatpak tools**: version check, `flatpak repair`, update, unused data removal
- **FWUPD integration**: list firmware devices, check firmware updates
- **File ownership**: `dnf repoquery -f` and `rpm -qf` lookups from a search field
- **DNF log tail** — read the last 500 lines of `/var/log/dnf.log` directly in the app
- **Fedora Magazine RSS** news feed — stay current without leaving the app
- **Backup RPM database** to a compressed `.tar.xz` archive
- **Export installed package lists** (full or explicitly-installed only)

### 🎨 UI & UX
- **GTK 4** native interface with adaptive theme support (light/dark follows system)
- **Resizable panes** with drag handles — tune the layout exactly to your workflow
- **Fullscreen mode** toggle (F11 / Esc)
- **Animated stack transitions** and smooth revealer sidebar
- **Overflow menu** with keyboard shortcut access (Menu key / Shift+F10)
- **Command history** — review every operation run during the session
- **Status bar + progress bar** for real-time feedback on long-running operations
- **Keyboard-friendly** design throughout
- Compatible with both **sudo** and **doas** for privilege escalation

---

## 📥 Installation

### Option 1 — RPM Package *(Fedora / RHEL / compatible)*

```bash
sudo dnf install https://github.com/almezali/pkger-8/releases/download/1.0.1/pkger-1.0.1-1.x86_64.rpm
```

Or download manually and install:

```bash
# Download
wget https://github.com/almezali/pkger-8/releases/download/1.0.1/pkger-1.0.1-1.x86_64.rpm

# Install
sudo dnf install ./pkger-1.0.1-1.x86_64.rpm
```

### Option 2 — AppImage *(any Linux distribution)*

```bash
# Download
wget https://github.com/almezali/pkger-8/releases/download/1.0.1/Pkger-x86_64.AppImage

# Make executable
chmod +x Pkger-x86_64.AppImage

# Run
./Pkger-x86_64.AppImage
```

> **Tip:** Use PKGER's own AppImage Manager to import and manage this file after first launch.

---

## 🔧 Requirements

| Component | Minimum |
|---|---|
| OS | Fedora Linux 40+ (or any RPM-based distribution) |
| GTK | 4.0+ |
| Python | 3.13+ *(only for source run)* |
| DNF | 5.x (`dnf5`) recommended, `dnf4` supported |
| Privilege tool | `sudo` or `doas` |
| Optional | `flatpak` for Flatpak features |
| Optional | `fwupdmgr` for firmware update detection |


---

## 🛡️ Security Model

- All privileged operations (install, remove, upgrade) require explicit **user confirmation** via dialog
- Privilege escalation is handled via **`sudo -S`** (password prompt in-app) or **`doas`** transparently
- No operations run silently in the background without user approval
- All commands are logged to the in-app **command history**

---

## 🤝 Contributing

Contributions, bug reports, and feature requests are welcome!

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/my-feature`
3. Commit your changes: `git commit -m 'Add my feature'`
4. Push to the branch: `git push origin feature/my-feature`
5. Open a Pull Request

---

## 📋 Changelog

### v1.0.1 — 2026
- Initial public release
- GTK 4 native UI (GTK 3 removed)
- DNF 5 (`dnf5`) primary backend with DNF 4 fallback
- Unified search across all package sources
- Security advisory enrichment for pending updates
- Full AppImage lifecycle management
- Repository presets (RPM Fusion Free + Nonfree)
- `sudo` and `doas` privilege escalation support

---

<div align="center">

Made with ❤️ for the Fedora Linux community

**[almezali](https://github.com/almezali)** · 2026

</div>
