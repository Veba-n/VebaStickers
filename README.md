<div align="center">

![VebaStickers Banner](https://cdn.modrinth.com/data/MXMlqbJb/images/3971841600b15193247ca937e68cdff7fefa0b16.png)

# VebaStickers — HD Chat Stickers & Emoji for Java & Bedrock

> **Send large, high-definition Telegram/WhatsApp-style stickers directly in Minecraft chat — fully server-side, no mods needed.**

VebaStickers is a modern, feature-rich Minecraft plugin that transforms your server's chat into a rich visual experience. Players can send large HD sticker images inline or as standalone messages, browse a beautiful GUI catalog, and manage their own favorites and language preferences — all with zero client-side installation.

Built from the ground up with **cross-platform cross-play** in mind: Java Edition and Bedrock Edition (via GeyserMC) players share the same seamless sticker experience.

</div>

---

## Core Features

### HD Sticker Rendering

<table align="center">
  <tr>
    <th style="text-align:center">Java Edition Chat</th>
  </tr>
  <tr>
    <td align="center"><img src="https://cdn.modrinth.com/data/cached_images/10b225cc6b6986abea4365b538329d29225445e2_0.webp" width="600" alt="Java chat ss"/></td>
  </tr>
</table>



- **Large standalone stickers** — Full-size HD image displayed in chat, rendered using custom font glyphs
- **Inline sticker codes** — Type `:sticker_name:` anywhere in chat to embed compact stickers mid-sentence
- **Auto-replacement** — Optionally convert classic emoticons (`:)`, `<3`, `:fire:`) into stickers automatically
- **Rich hover tooltips** — Hovering a sticker in chat shows a detailed tooltip with sticker name, author and pack info
- **Click-to-use** — Clicking a sticker in chat suggests the sticker command for quick reuse

### Cross-Platform: Java + Bedrock

<table align="center">
  <tr>
    <th style="text-align:center">Bedrock Edition Chat</th>
  </tr>
  <tr>
    <td align="center"><img src="https://cdn.modrinth.com/data/cached_images/5cd95a19e936a7bb62b6c16e6ad33924a2d93b7c.jpeg" width="600" alt="Bedrock chat ss"/></td>
  </tr>
</table>


- **GeyserMC + Floodgate support** — Full native integration; Bedrock mobile players can browse and send stickers via the Emote button menu
- **Automatic Bedrock pack generation** — `.mcpack` file generated and pushed to Geyser's pack folder on every startup automatically
- **Bedrock native form UI** — Mobile/console players get a touch-friendly Bedrock form menu instead of a Java inventory GUI
- **Geyser Emote button shortcut** — Tap the Emote button on Bedrock to instantly open the sticker catalog
### GUI Catalog & Browsing

<table align="center">
  <tr>
    <th style="text-align:center">Java Edition GUI</th>
    <th style="text-align:center">Bedrock Edition UI</th>
  </tr>
  <tr>
    <td align="center"><img src="https://cdn.modrinth.com/data/cached_images/23090b6e27219f7f0e0f9f71579bf97909b299f0.png" width="300"/></td>
    <td align="center"><img src="https://cdn.modrinth.com/data/cached_images/b9ae74ae180bacd0a60c4e09ec2da1e39be595ca.jpeg" width="300"/></td>
  </tr>
  <tr>
    <td align="center"><img src="https://cdn.modrinth.com/data/cached_images/39801bc2433d31918fef6b1d99171d49e11eab41.png" width="300"/></td>
    <td align="center"><img src="https://cdn.modrinth.com/data/cached_images/2a48ce478b846548752006c7a67370b73ec956bd.jpeg" width="300"/></td>
  </tr>
  <tr>
    <td align="center"><img src="https://cdn.modrinth.com/data/cached_images/63b6eea0b66e0b5da2f84aa09d0637d591373a6d.png" width="300"/></td>
    <td align="center"><img src="https://cdn.modrinth.com/data/cached_images/aa11a209d9d7844634d493f92a30994543325c2d.jpeg" width="300"/></td>
  </tr>
</table>

- **Interactive chest GUI** (`/sticker`) — Browse all sticker packs and categories from a single polished inventory menu
- **Category filtering** — Stickers are organized into named categories; browse by category from the menu
- **Live search** — Type `/sticker search <query>` or use the in-GUI search bar to find stickers by name instantly
- **Favorites system** — Players can bookmark their favorite stickers for one-tap access via `/sticker favorites`
- **Locked sticker previews** — Players can preview stickers they don't have permission for (greyed out), encouraging VIP purchases

### 16-Language i18n Support
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


<table align="center">
  <tr>
    <th style="text-align:center">languages</th>
  </tr>
  <tr>
    <td align="center"><img src="https://cdn.modrinth.com/data/cached_images/1de8f576ac95c9aff6a00fca65795bc83e282ff6.png" width="600" alt="languages"/></td>
  </tr>
</table>

### Sticker Packs & Permissions
- **Pack-based permissions** — Each sticker category maps to a permission node (`sticker.pack.<name>`)
- **LuckPerms integration** — Assign packs to ranks; players see only what they have access to
- **VIP / Premium packs** — Separate high-tier sticker collections for subscriber or donation ranks
- **Per-sticker permissions** — Fine-grained control: grant or revoke individual stickers

### Admin Tools

| Admin Dashboard | Admin Dashboard 2 |
| :---: | :---: |
| ![Admin gui 1](https://cdn.modrinth.com/data/cached_images/fbbb28ab6f38738c62c7c8919ce0ab0548f96dd4.png) | ![Admin gui 2](https://cdn.modrinth.com/data/cached_images/88e573e0aa9495fa01b2dfbbcf845a61f2b5e2ad.png) |

- **Full Admin GUI** (`/stickeradmin gui`) — Visual dashboard with live statistics, pack management, and player controls
- **Add stickers in-game** — Upload new stickers directly via admin command; HD image processed and pack recompiled automatically
- **Remove stickers in-game** — Delete stickers and recompile the resource pack without server restarts
- **Import sticker packs** — Bulk-import a zip of images into a new category in seconds
- **Export Bedrock pack** — Manually trigger `.mcpack` regeneration and re-push to Geyser via `/stickeradmin exportbedrock`
- **Player ban system** — Ban specific players from using stickers (`/stickeradmin ban <player>`) with reasons
- **Force resource pack resend** — Send updated pack to individual players or everyone via `/stickeradmin sendpack`
- **Live reload** — Reload all configs, sticker definitions, and language packs without restarting (`/stickeradmin reload`)

### Floating 3D Hologram Stickers *(Java Edition)*


<table align="center">
  <tr>
    <th style="text-align:center">Sticker Hologram</th>
  </tr>
  <tr>
    <td align="center"><img src="https://cdn.modrinth.com/data/cached_images/913636a8fa6af0b70ed7965837fc83188da0f084_0.webp" width="600" alt="Sticker Hologram"/></td>
  </tr>
</table>

- When a sticker is sent, a **floating 3D hologram** of the sticker image appears above the sender's head
- Billboard display — always faces all viewers
- Gentle bob animation while floating
- Automatically hides from the sender's own view (doesn't obstruct screen)
- Configurable scale, duration, and height offset

### Economy Integration
- **Vault support** — Charge players in-game currency per sticker use or per pack unlock
- **PlayerPoints support** — Alternative economy point system fully supported
- Configurable pricing per pack or per sticker category

### Built-in Micro HTTP Server
- **Zero external dependency** — The plugin runs its own lightweight web server to serve the resource pack automatically
- No Nginx, no Dropbox, no external URL required — just install and go
- Automatically detects the server's public IP and builds the download URL

### Audio Feedback
- Configurable sound effect plays when a sticker is sent
- Separate sounds for send success, GUI click, and purchase events

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

### Minecraft Version & Cross-Version Support

VebaStickers is engineered as a **single, unified JAR** that works out-of-the-box across server and client versions — supporting both legacy `1.16.5` releases and Minecraft's new year-based calendar releases (**25.x, 26.x+**).

| Component | Supported Versions | Status & Details |
|---|---|---|
| **Minecraft Server** | **1.16.5 – 26.x+** | Native support for Paper, Purpur, Folia, and Spigot. |
| **Java Clients** | **1.16.x – 26.x+** | Full native support (and via ViaVersion / ViaBackwards). |
| **Bedrock Clients** | **All Recent Versions** | Fully supported via **GeyserMC & Floodgate**. |

#### Single-JAR Multi-Version Architecture:
- **Dual Chat Engines (Paper + Spigot):** Automatically detects server software at runtime. Uses Paper's `AsyncChatEvent` on Paper/Purpur, and safely falls back to `AsyncPlayerChatEvent` on pure Spigot.
- **Dual Resource Pack Generation:** Simultaneously compiles modern 1.21.4+ / 25.x / 26.x+ `items/paper.json` model paths AND legacy 1.16–1.20 `models/item/paper.json` override definitions.
- **Universal Pack Format Range (`[6, 99]`):** Covers pack_format definitions from legacy MC 1.16.5 up to formats 50+ in year 2026 drops (26.x), preventing "Incompatible Pack" warnings.
- **Class-Safe Feature Guarding:** Modern visual APIs like 3D `TextDisplay` floating holograms automatically detect server capabilities and fallback safely on older 1.16–1.19.3 servers without throwing errors.
- **Zero Configuration Required:** Drop `VebaStickers.jar` into your `plugins/` directory on any 1.16.5 – 26.x+ server and it works out of the box.

---

## Commands

| Command | Description |
|---|---|
| `/sticker` or `/stickers` | Open the main sticker GUI catalog |
| `/sticker send <id>` | Send a specific sticker by its code |
| `/sticker search <query>` | Search stickers by name |
| `/sticker favorites` | Open your personal favorites list |
| `/sticker lang [code\|list]` | Change your language or list available languages |
| `/sticker toggle` | Toggle sticker visibility for yourself |
| `/sticker pack` | Manually trigger resource pack download |
| `/sticker help` | Show command help menu |
| `/sbook` | Open sticker catalog as a book-style GUI |
| `/stickeradmin gui` | Open the admin dashboard GUI |
| `/stickeradmin add <id> <url>` | Add a new sticker from a URL |
| `/stickeradmin remove <id>` | Remove a sticker and recompile pack |
| `/stickeradmin import <pack>` | Bulk-import sticker pack from zip |
| `/stickeradmin give <player> <pack>` | Grant a sticker pack to a player |
| `/stickeradmin ban <player>` | Ban a player from using stickers |
| `/stickeradmin sync` | Regenerate resource pack and SHA-1 |
| `/stickeradmin exportbedrock` | Regenerate and push Bedrock .mcpack |
| `/stickeradmin status` | Display detailed system status, server engine, and player pack health |
| `/stickeradmin verify` | Run a 6-point integrity check on stickers, models, and HTTP server |
| `/stickeradmin reload` | Reload all plugin configurations |

---

## Permissions

| Permission | Default | Description |
|---|---|---|
| `sticker.gui` | **everyone** | Open the sticker catalog GUI |
| `sticker.use` | **everyone** | Send stickers in chat |
| `sticker.use.*` | OP | Send all stickers without pack restrictions |
| `sticker.pack.<name>` | OP | Access a specific named sticker pack |
| `sticker.category.*` | OP | Access all sticker categories |
| `sticker.bypass.cooldown` | OP | Skip the sticker cooldown |
| `sticker.admin` | OP | Access all admin commands and GUI |

---

## FAQ

**Does this require any client-side mod or resource pack installation?**
The plugin automatically delivers the resource pack to players on join — no manual installation required. Players on vanilla Java or Bedrock clients see everything correctly.

**Does it work on Bedrock / Mobile / Console?**
Yes. VebaStickers has first-class GeyserMC and Floodgate integration. Bedrock players get a native touch-UI form menu, and the Bedrock `.mcpack` is generated and pushed automatically. They can browse, send, and receive stickers seamlessly.

**Can I add my own stickers?**
Yes. Use `/stickeradmin add <id> <image-url>` to add any PNG image as an HD sticker. The resource pack is recompiled and re-served instantly — no server restart needed.

**Can I import a full sticker pack at once?**
Yes. Use `/stickeradmin import <zip>` to bulk-import a zip file of images. All stickers are automatically processed, sliced, and registered under a new category.

**How does the inline `:sticker_code:` syntax work?**
When `inline-stickers-enabled: true` is set (default), VebaStickers intercepts chat messages and replaces `:code:` patterns with the corresponding sticker glyph in real time.

**Does this affect server performance?**
VebaStickers is designed for minimal overhead. Image processing only happens when stickers are added or the pack is compiled — never during normal gameplay. Chat processing is a lightweight string scan.

**Can I restrict stickers to premium ranks?**
Yes. Create sticker categories with permission nodes (`sticker.pack.<name>`) and assign those permissions to your VIP/Donor ranks via LuckPerms. Free players will see locked sticker previews but cannot use them.

**Is the floating hologram visible to Bedrock players?**
The 3D floating hologram is a Java Edition exclusive visual feature. It uses Java's `TextDisplay` entity which Geyser cannot reliably render at scale on mobile. Bedrock players see the chat sticker normally.

**Can players opt out of seeing others' stickers?**
Yes. Players can toggle sticker visibility for themselves via `/sticker toggle`.

**Does it support multi-language servers?**
Fully. 16 languages are bundled. Each player's UI, messages, and notifications are served in their own language automatically based on their Minecraft client locale. Players can also manually choose with `/sticker lang <code>`.

---

## License & Usage

Copyright (c) Veba. All Rights Reserved.  
VebaStickers is provided as a compiled plugin release. Unauthorized redistribution, modification, or re-hosting of binary JAR files without prior written consent is strictly prohibited.

---

<div align="center">

[![GitHub](https://img.shields.io/badge/Source-GitHub-181717?style=flat-square&logo=github)](https://github.com/Veba-n/VebaStickers)
[![Modrinth](https://img.shields.io/badge/Modrinth-VebaStickers-00AF5C?style=flat-square&logo=modrinth)](https://modrinth.com/plugin/vebastickers)

</div>
