# 🌀 KroxyTpa — Premium TPA Plugin

> Smooth teleportation system for Spigot / Paper / Purpur with gradient chat UI, clickable buttons, GUI menus, TPA ban system, countdown teleport & move-cancel protection.

![Version](https://img.shields.io/badge/version-1.0.0-FF0072?style=for-the-badge)
![MC Versions](https://img.shields.io/badge/minecraft-1.19--1.21.11-22FF00?style=for-the-badge)
![Platform](https://img.shields.io/badge/platform-Spigot%20%7C%20Paper%20%7C%20Purpur-blue?style=for-the-badge)
![License](https://img.shields.io/badge/license-MIT-yellow?style=for-the-badge)

---

## ✨ Features

- 📩 **TPA Requests** — Send, accept, deny and cancel teleport requests
- 🖱️ **Clickable Buttons** — Accept / Deny / Cancel buttons directly in chat
- 🖼️ **GUI Menus** — Beautiful inventory GUI for TPA management
- ⏳ **Countdown Teleport** — Configurable countdown before teleport
- 🚫 **Move Cancel** — Moving during countdown cancels teleport with big screen title
- 🔨 **TPA Ban System** — Ban players from using TPA with time & reason
- 🎨 **Gradient UI** — Colorful gradient chat prefix and messages
- 🔔 **Action Bar** — Live countdown shown on action bar
- 🔊 **Sounds** — Sound effects on request, accept, deny, teleport
- ⚙️ **Fully Configurable** — All messages, cooldowns, sounds via `config.yml`
- 🔗 **LuckPerms Support** — Full permission node support
- 🔄 **Instant Reload** — `/kroxytpa reload` — no restart needed

---

## 🖥️ Supported Platforms

| Platform | Supported |
|----------|-----------|
| Paper | ✅ |
| Spigot | ✅ |
| Purpur | ✅ |
| Bukkit | ✅ |
---

---

## 📦 Installation

1. Download `KroxyTpa.jar` from [Releases](../../releases)
2. Place it in your server's `/plugins` folder
3. Start/restart your server
4. Configure in `/plugins/KroxyTpa/config.yml`
5. Run `/kroxytpa reload` after any config changes

---

## 📜 Commands

### 👤 Player Commands

| Command | Aliases | Description |
|---------|---------|-------------|
| `/tpa <player>` | — | Send a TPA request |
| `/tpahere <player>` | — | Request player to come to you |
| `/tpaaccept [player]` | `/tpaccept` `/tpyes` | Accept a TPA request |
| `/tpadeny [player]` | — | Deny a TPA request |
| `/tpacancel [player\|all]` | `/tpcancel` | Cancel your TPA request |
| `/tpaall` | — | Send TPA to all online players |
| `/tpalist` | `/tplist` | View pending requests |

### 👑 Admin Commands

| Command | Aliases | Description |
|---------|---------|-------------|
| `/tphere <player>` | — | Silently teleport a player to you |
| `/tpall` | — | Silently teleport ALL players to you |
| `/tp <player>` | — | Silently teleport to a player |
| `/tpaban <player> <time> [reason]` | `/tpabanlist` | TPA ban a player |
| `/kroxytpa [on\|off\|reload\|menu]` | `/ktpa` | Admin control panel |

---

## 🔐 Permissions

### 👤 Player Permissions

| Permission | Default | Description |
|------------|---------|-------------|
| `kroxytpa.tpa` | false | Use /tpa |
| `kroxytpa.tpahere` | false | Use /tpahere |
| `kroxytpa.tpaaccept` | false | Use /tpaaccept |
| `kroxytpa.tpadeny` | false | Use /tpadeny |
| `kroxytpa.tpacancel` | false | Use /tpacancel |
| `kroxytpa.tpaall` | false | Use /tpaall |
| `kroxytpa.tpalist` | false | Use /tpalist |

### 👑 Admin Permissions

| Permission | Default | Description |
|------------|---------|-------------|
| `kroxytpa.admin` | OP | Full admin control |
| `kroxytpa.admin.tphere` | OP | Use /tphere |
| `kroxytpa.admin.tpall` | OP | Use /tpall |
| `kroxytpa.admin.tp` | OP | Use /tp |
| `kroxytpa.admin.ban` | OP | Use /tpaban |
| `kroxytpa.bypass` | OP | Bypass all cooldowns & move-cancel |
| `kroxytpa.bypass-cooldown` | OP | Bypass send cooldown only |
| `kroxytpa.*` | OP | All permissions |

> 💡 Assign player permissions via **LuckPerms** or any permission plugin.

---

## 👤 Author

**Made with ❤️ by Kroxy**
🌐 [www.kroxy.org](https://www.kroxy.org)

---
