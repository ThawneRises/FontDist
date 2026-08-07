# 🎨 FontCraft Assets Library

> **Central Asset Repository for FontCraft Module**
> Your dynamic font and emoji library for seamless WebUI integration.

<div align="center">

[![Last Commit](https://img.shields.io/github/last-commit/ThawneRises/FontDist)](https://github.com/ThawneRises/FontDist/commits/Master) [![Build Status](https://github.com/ThawneRises/FontDist/actions/workflows/reconfigure.yml/badge.svg)](https://github.com/ThawneRises/FontDist/actions/workflows/reconfigure.yml)

<br>

**[ 📖 View Visual Catalog ](Preview.md)** &nbsp;&nbsp;•&nbsp;&nbsp; **[ ⚡ Main FontCraft Module ](https://github.com/RipperHybrid/FontCraft.git)**

</div>

---

This repository serves as the remote asset database for the **FontCraft** module, hosting font files, emoji packs, and metadata that enable dynamic fetching and display within the WebUI.

## 🚀 Why Separate Assets?

- **Lightweight Installation**: Keep the main module zip small and efficient.
- **Infinite Expansion**: Add unlimited fonts/emojis without module updates.
- **Dynamic Updates**: Assets become available immediately to all users.
- **Centralized Management**: Single source of truth for all font assets.

## ⚡ Automated Metadata System

### 🤖 How It Works

**Workflow Triggers:**
* Push to `Master` branch (excluding auto-generated tracking files).
* Manual trigger via `workflow_dispatch`.
* Modifications to `Fonts/` or `Emoji/` directories.

**Automation Process:**
1. **Verify**: Recursively scans and checks for new or modified `.ttf` assets.
2. **Patch**: Automatically runs FontForge to inject missing UI glyphs into unpatched fonts.
3. **Render**: Utilizes Skia and Pillow to generate crisp `.png` visual previews for each font.
4. **Generate**: Creates the structured JSON API and the visual Markdown catalog.
5. **Deploy**: Commits the generated preview images, updated `patched.json`, and metadata back to the repository.

### 📊 Generated Files

| File | Purpose | Format |
| --- | --- | --- |
| [fonts.json](fonts.json) | Module / WebUI API endpoint | Structured JSON |
| [patched.json](patched.json) | Tracks glyph patching states to prevent redundant builds | JSON |
| [Preview.md](Preview.md) | Visual catalog | Markdown with images |

> **Note**: Main Module: [FontCraft](https://github.com/RipperHybrid/FontCraft.git) on GitHub.

## 📁 Repository Structure

```text
FontDist/
├── Emoji/                   # Emoji Packs & Icon Fonts
│   └── [Emoji Pack Name]/
│       └── font.ttf         # Font file (PNG auto-generates)
│
├── Fonts/                   # System & Display Fonts
│   └── [Font Family Name]/
│       └── font.ttf         # Font file (PNG auto-generates)
│
├── fonts.json               # Module & WebUI API Metadata
├── patched.json             # Patching State Tracker
├── Preview.md               # Visual Catalog
└── .github/workflows/       # Automation Scripts

```

## 🔗 Credits & Attributions

> [!note]
> All fonts and emojis belong to their respective creators. This repository acts as a distribution point for legally shareable assets. The automated patching process does not claim ownership or alter the original font's identity. If you're a copyright holder and wish to have your content removed, please contact the maintainer on Telegram.