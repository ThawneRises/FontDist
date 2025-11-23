# 🎨 FontCraft Assets Library

> **Central Asset Repository for FontCraft Module**  
> Your dynamic font and emoji library for seamless WebUI integration.

This repository serves as the remote asset database for the **FontCraft** module, hosting font files, emoji packs, and metadata that enable dynamic fetching and display within the WebUI.

## 🚀 Why Separate Assets?

- **Lightweight Installation**: Keep the main module zip small and efficient
- **Infinite Expansion**: Add unlimited fonts/emojis without module updates
- **Dynamic Updates**: Assets become available immediately to all users
- **Centralized Management**: Single source of truth for all font assets

## 📁 Repository Structure

```

FontCraft-Assets/
├──Emoji/                    # Emoji Packs & Icon Fonts
│└── [Emoji Pack Name]/
│├── font.ttf          # Font file (.ttf or .otf)
│└── preview.png       # Visual preview
│
├──Fonts/                    # System & Display Fonts
│└── [Font Family Name]/
│├── font.ttf          # Font file (.ttf or .otf)
│└── preview.png       # Style preview
│
├──template/                 # Folder to store template for webui
│└── template.zip          # Template for webui module creation
│
├──fonts.json                # AUTO-GENERATED: Module & WebUI API Metadata
├──Preview.md                # AUTO-GENERATED: Visual Catalog
└──.github/workflows/        # Automation Scripts

```

## ⚡ Automated Metadata System

### 🤖 How It Works

**Workflow Triggers:**
- Push to `Master` branch (excluding metadata files)
- Manual trigger via `workflow_dispatch`
- Modifications to `Fonts/` or `Emoji/` directories

**Automation Process:**
1. **Scan**: Recursively searches for `.ttf`, `.otf`, and `.png` files
2. **Generate**: Creates structured JSON API and visual catalog
3. **Deploy**: Automatically commits updated metadata back to repository

### 📊 Generated Files

| File | Purpose | Format |
|------|---------|---------|
| [fonts.json](fonts.json) | Module/WebUI API endpoint | Structured JSON |
| [Preview.md](Preview.md) | Visual catalog | Markdown with images |

> **Note**: Main Module: FontCraft on GitHub - The account which has the module is suspended for now.

## 🔗 Credits
- **jq Binary** – [jq](https://jqlang.org) `# Stored in template zip`
- **zip Binary** – [zip](https://infozip.sourceforge.net) `# Stored in template zip`

## 👨‍💻 Maintainer

- **AshBorn** – [@Ripper_Hybrid](https://t.me/Ripper_Hybrid)