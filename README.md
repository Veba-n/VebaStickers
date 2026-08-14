# VebaStickers — Universal HD Chat Stickers for Minecraft

[![Latest Release](https://img.shields.io/badge/Release-v1.0.0-blue?style=flat-square&logo=github)](https://github.com/Veba-n/VebaStickers/releases)
[![Minecraft Version](https://img.shields.io/badge/Minecraft-1.16.5--26.x%2B-orange?style=flat-square&logo=minecraft)](https://modrinth.com/plugin/vebastickers)
[![Modrinth Downloads](https://img.shields.io/badge/Modrinth-Available-00AF5C?style=flat-square&logo=modrinth)](https://modrinth.com/plugin/vebastickers)
[![Compatibility](https://img.shields.io/badge/Platform-Paper%20%7C%20Spigot%20%7C%20Geyser-purple?style=flat-square)](https://github.com/Veba-n/VebaStickers)
[![License](https://img.shields.io/badge/License-All%20Rights%20Reserved-red?style=flat-square)](LICENSE)

> **The ultimate single-JAR cross-platform sticker plugin for Minecraft (Java & Bedrock).**  
> Send HD Telegram/WhatsApp-style stickers inline or standalone directly in Minecraft chat — fully server-side with zero client-side mod requirements.

---

## Table of Contents

- [Core Features](#core-features)
- [Multi-Language Support](#multi-language-support-16-client-aware-locales)
- [Single-JAR Architecture](#single-jar-multi-version-architecture)
- [Download & Installation](#download--installation)
- [Modrinth & Release Channels](#modrinth--release-channels)
- [Compatibility & Integrations](#compatibility--integrations)
- [Commands](#commands)
- [Permissions & LuckPerms](#permissions--luckperms)
- [Frequently Asked Questions](#frequently-asked-questions)
- [Support & Issue Tracker](#support--issue-tracker)
- [License & Usage](#license--usage)

---

## Core Features

### HD Inline & Standalone Chat Stickers
- **Standalone HD Display:** Full-size high-definition images rendered cleanly in chat using custom font glyphs.
- **Inline Stickers:** Use `:sticker_name:` anywhere inside chat messages to embed compact stickers mid-sentence.
- **Auto Emoticon Conversion:** Automatically transform classic smilies (`:)`, `<3`, `:fire:`) into stickers.
- **Rich Hover & Interactive Tooltips:** Hovering a sticker shows its name, pack author, and click-to-reuse prompt.

### Cross-Platform Cross-Play (Java + Bedrock)
- **GeyserMC & Floodgate Integration:** Bedrock mobile, console, and Windows 10/11 players share the same visual experience.
- **Automatic `.mcpack` Exporter:** Generates and deploys the Bedrock resource pack to Geyser automatically on server startup.
- **Bedrock Touch Form UI:** Bedrock players get a native, responsive Form UI menu instead of a Java inventory GUI.
- **Geyser Emote Button Shortcut:** Double-tap sneak or tap the Emote button on mobile to open the sticker menu instantly.

### GUI Catalog & Search Engine
- **WhatsApp-Style GUI (`/sticker`):** Browse categories, recent stickers, and personal favorites.
- **Live Search Bar:** Search any sticker by name in real time (`/sticker search <query>`).
- **Personal Favorites:** Bookmark stickers for one-tap sending.
- **VIP Locked Previews:** Players can preview locked stickers, driving rank upgrades.

### Floating 3D Hologram Stickers (Java Edition)
- When a sticker is sent, a floating 3D hologram of the sticker image appears above the sender's head.
- Billboard display: always faces all viewers.
- Gentle bob animation while floating.
- Automatically hides from the sender's own view (doesn't obstruct screen).
- Configurable scale, duration, and height offset.

### Built-in Micro HTTP Server
- **Zero external dependency:** The plugin runs its own lightweight web server to serve the resource pack automatically.
- No Nginx, no Dropbox, no external URL required — just install and go.
- Automatically detects the server's public IP and builds the download URL.

---

## Multi-Language Support (16 Client-Aware Locales)

All player-facing messages are fully localized. Players automatically receive messages in their own language (auto-detected from their Minecraft client locale), or they can manually select via `/sticker lang`:

| Language | Code | Language | Code |
|---|---|---|---|
| English | `en` | Türkçe | `tr` |
| Deutsch | `de` | Español | `es` |
| Français | `fr` | Português | `pt` |
| Русский | `ru` | 中文 | `zh` |
| 日本語 | `ja` | 한국어 | `ko` |
| Italiano | `it` | Nederlands | `nl` |
| Polski | `pl` | العربية | `ar` |
| हिन्दी | `hi` | Українська | `uk` |

---

## Single-JAR Multi-Version Architecture

VebaStickers is engineered as a unified JAR that works out-of-the-box across server and client versions — supporting both legacy 1.x releases and Minecraft's new year-based calendar releases (**25.x, 26.x+**).

- **Dual Chat Engines (Paper + Spigot):** Automatically detects server software at runtime. Uses Paper's `AsyncChatEvent` on Paper/Purpur/Folia, and safely falls back to `AsyncPlayerChatEvent` on pure Spigot.
- **Dual Resource Pack Generation:** Simultaneously compiles modern 1.21.4+ / 25.x / 26.x+ `items/paper.json` model paths AND legacy 1.16–1.20 `models/item/paper.json` override definitions.
- **Universal Pack Format Range (`[6, 99]`):** Covers pack_format definitions from legacy MC 1.16.5 up to formats 50+ in year 2026 drops (26.x), preventing "Incompatible Pack" warnings.
- **Class-Safe Feature Guarding:** Modern visual APIs like 3D `TextDisplay` floating head holograms automatically detect server capabilities and fallback safely on older 1.16–1.19.3 servers without throwing errors.

---

## Download & Installation

### Option A: From GitHub Releases (Official Compiled JAR)
1. Navigate to the [GitHub Releases Page](https://github.com/Veba-n/VebaStickers/releases).
2. Download the latest release (`VebaStickers-1.0.0.jar`).
3. Place the `.jar` file into your server's `plugins/` directory.
4. Restart your server.

### Option B: From Modrinth
You can also download verified production builds directly from our [Modrinth Store Page](https://modrinth.com/plugin/vebastickers) (or [Modrinth Project Page](https://modrinth.com/project/vebastickers)).

```
plugins/
 └── VebaStickers-1.0.0.jar
```

---

## Modrinth & Release Channels

| Channel | Platform | Artifact | Target Audience |
|---|---|---|---|
| **GitHub Releases** | [GitHub Releases](https://github.com/Veba-n/VebaStickers/releases) | `VebaStickers-1.0.0.jar` | Official compiled releases & updates |
| **Modrinth Store** | [Modrinth Plugin Page](https://modrinth.com/plugin/vebastickers) | `VebaStickers.jar` | Public community releases |
| **Bedrock Pack** | Server auto-generated | `VebaStickers_Bedrock.mcpack` | GeyserMC auto-push asset |

---

## Compatibility & Integrations

| Software | Status | Notes |
|---|---|---|
| **Paper / Purpur / Folia** | Native Engine | High-performance AsyncChatEvent + ChatRenderer |
| **Vanilla Spigot / CraftBukkit** | Native Engine | Automatic fallback to AsyncPlayerChatEvent engine |
| **GeyserMC** | Native Integration | Bedrock form UI, .mcpack auto-push |
| **Floodgate** | Native Integration | Player detection & cross-play |
| **LuckPerms** | Integrated | Per-rank sticker pack permissions |
| **Vault** | Integrated | Economy charging per sticker |
| **PlayerPoints** | Integrated | Alternative point economy |
| **PlaceholderAPI** | Integrated | Expose sticker stats as placeholders |
| **ViaVersion / ViaBackwards** | Compatible | Multi-version client support |

---

## Commands

### Player Commands
| Command | Permission | Description |
|---|---|---|
| `/sticker` | `sticker.gui` | Open main sticker GUI catalog |
| `/sticker send <id>` | `sticker.use` | Send a specific sticker by code |
| `/sticker search <query>` | `sticker.use` | Search stickers by name |
| `/sticker favorites` | `sticker.use` | Open favorite stickers list |
| `/sticker lang [code]` | `sticker.use` | Select language preference |
| `/sticker toggle` | `sticker.use` | Toggle sticker chat visibility |
| `/sticker pack` | `sticker.use` | Request resource pack download |
| `/sbook` | `sticker.gui` | Open sticker catalog as a book GUI |

### Admin Commands
| Command | Permission | Description |
|---|---|---|
| `/stickeradmin gui` | `sticker.admin` | Open interactive admin dashboard |
| `/stickeradmin add <id> <url>` | `sticker.admin` | Add new sticker from image URL |
| `/stickeradmin remove <id>` | `sticker.admin` | Remove a sticker and recompile pack |
| `/stickeradmin import <pack>` | `sticker.admin` | Bulk-import sticker pack from zip archive |
| `/stickeradmin status` | `sticker.admin` | Display server engine, HTTP, and SHA-1 status |
| `/stickeradmin verify` | `sticker.admin` | Run 6-point integrity & health check |
| `/stickeradmin exportbedrock` | `sticker.admin` | Regenerate and push `.mcpack` to Geyser |
| `/stickeradmin reload` | `sticker.admin` | Reload all configurations and languages |

---

## Permissions & LuckPerms

| Permission | Default | Description |
|---|---|---|
| `sticker.gui` | Everyone | Open the sticker catalog GUI |
| `sticker.use` | Everyone | Send stickers in chat |
| `sticker.use.*` | OP | Send all stickers without pack restrictions |
| `sticker.pack.<name>` | OP | Access a specific named sticker pack |
| `sticker.category.*` | OP | Access all sticker categories |
| `sticker.bypass.cooldown` | OP | Skip the sticker cooldown |
| `sticker.admin` | OP | Access all admin commands and GUI |

### LuckPerms Command Examples
```bash
# Grant VIP sticker category to VIP group:
/lp group vip permission set sticker.pack.vip true

# Grant specific sticker permission to a player:
/lp user PlayerName permission set sticker.use.fire_crown true

# Grant cooldown bypass:
/lp group mvp permission set sticker.bypass.cooldown true
```

---

## Frequently Asked Questions

**Does this require any client-side mod or resource pack installation?**  
The plugin automatically delivers the resource pack to players on join — no manual installation required. Players on vanilla Java or Bedrock clients see everything correctly.

**Does it work on Bedrock / Mobile / Console?**  
Yes. VebaStickers has first-class GeyserMC and Floodgate integration. Bedrock players get a native touch-UI form menu, and the Bedrock `.mcpack` is generated and pushed automatically.

**Can I add my own stickers?**  
Yes. Use `/stickeradmin add <id> <image-url>` to add any PNG image as an HD sticker. The resource pack is recompiled and re-served instantly — no server restart needed.

**Can I import a full sticker pack at once?**  
Yes. Use `/stickeradmin import <zip>` to bulk-import a zip file of images.

---

## Support & Issue Tracker

Need assistance or wish to report a bug?

- [Report an Issue](https://github.com/Veba-n/VebaStickers/issues/new?template=bug_report.md) — Provide output from `/stickeradmin status` and server logs.
- [Feature Suggestion](https://github.com/Veba-n/VebaStickers/issues/new?template=feature_request.md) — Suggest features or integrations.

---

## License & Usage

Copyright (c) Veba. All Rights Reserved.  
This software is provided as a compiled plugin release. Unauthorized redistribution, modification, or re-hosting of binary JAR files without prior written consent is strictly prohibited.
