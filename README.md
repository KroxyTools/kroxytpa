# 🌀 KroxyTpa — Premium TPA Plugin

> Smooth teleportation system for Spigot / Paper / Purpur with gradient chat UI, clickable buttons, GUI menus, TPA ban system, countdown teleport & move-cancel protection.

![Version](https://img.shields.io/badge/version-1.0.0-FF0072?style=for-the-badge)
![MC Versions](https://img.shields.io/badge/minecraft-1.13--1.21.11-22FF00?style=for-the-badge)
![Platform](https://img.shields.io/badge/platform-Spigot%20%7C%20Paper%20%7C%20Purpur-blue?style=for-the-badge)
![Java](https://img.shields.io/badge/java-8+-orange?style=for-the-badge)
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
| BungeeCord / Velocity | ❌ |
| Fabric / Forge | ❌ |

---

## 📋 Supported Versions

```
1.13 · 1.13.1 · 1.13.2
1.14 · 1.14.1 · 1.14.2 · 1.14.3 · 1.14.4
1.15 · 1.15.1 · 1.15.2
1.16 · 1.16.1 · 1.16.2 · 1.16.3 · 1.16.4 · 1.16.5
1.17 · 1.17.1
1.18 · 1.18.1 · 1.18.2
1.19 · 1.19.1 · 1.19.2 · 1.19.3 · 1.19.4
1.20 · 1.20.1 · 1.20.2 · 1.20.3 · 1.20.4 · 1.20.6
1.21 · 1.21.1 · 1.21.2 · 1.21.3 · 1.21.4 · 1.21.11
```

> ❌ 1.12.2 and below — NOT supported

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

## ⚙️ Configuration

```yaml
settings:
  countdown-seconds:      5      # Seconds before teleport
  request-expire-seconds: 60     # Request auto-expire time
  cancel-on-move:         true   # Cancel teleport if player moves
  max-pending-requests:   5      # Max outgoing requests per player
  sounds-enabled:         true   # Enable/disable sounds
  tpa-cooldown:           0      # Cooldown between requests (0 = off)
```

Full config → [`src/main/resources/config.yml`](src/main/resources/config.yml)

---

## 🔨 TPA Ban Examples

```bash
/tpaban Steve 1h Spamming        # Ban for 1 hour
/tpaban Steve 30m                # Ban for 30 minutes
/tpaban Steve 7d Abusing TPA     # Ban for 7 days
/tpaban Steve 0                  # Permanent ban
/tpaban unban Steve              # Unban
/tpaban list                     # View all active bans
```

---

## 🏗️ Building from Source

```bash
git clone https://github.com/YourUsername/KroxyTpa.git
cd KroxyTpa
mvn clean package
# Output: target/KroxyTpa.jar
```

**Requirements:** Java 8+, Maven 3.6+

---

## 📁 Project Structure

```
KroxyTpa/
├── src/main/java/me/kroxytpa/kroxytpa/
│   ├── KroxyTpa.java              # Main plugin class
│   ├── TpaRequest.java            # TPA request model
│   ├── commands/
│   │   └── CommandHandler.java    # All command handling
│   ├── gui/
│   │   ├── KroxyTpaGui.java       # Main TPA GUI
│   │   ├── BanListGui.java        # Ban list GUI
│   │   └── BanConfirmGui.java     # Ban confirm GUI
│   ├── listeners/
│   │   ├── GuiClickListener.java
│   │   ├── BanGuiClickListener.java
│   │   ├── CooldownChatListener.java
│   │   └── PlayerMoveListener.java
│   ├── managers/
│   │   ├── TpaManager.java        # Core TPA logic
│   │   ├── BanManager.java        # Ban system
│   │   └── DataManager.java       # SQLite data storage
│   └── utils/
│       └── GradientUtil.java      # Color/gradient parsing
└── src/main/resources/
    ├── config.yml                 # Default configuration
    └── plugin.yml                 # Plugin metadata
```

---

## 👤 Author

**Made with ❤️ by Kroxy**
🌐 [www.kroxy.org](https://www.kroxy.org)

---

> ⚠️ Requires Minecraft 1.13+ · Java 8+
