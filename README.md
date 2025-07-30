
# 🌊 SeaweedClear 

[![Java](https://img.shields.io/badge/Java-8%2B-orange?logo=openjdk)](https://java.com)
[![Spigot](https://img.shields.io/badge/Spigot-1.13%2B-yellow)](https://www.spigotmc.org)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![GitHub Stars](https://img.shields.io/github/stars/username/repo)](https://github.com/username/repo/stargazers)
[![Discord](https://img.shields.io/discord/server_id?logo=discord&label=Discord)](https://discord.gg/invite-link)

The ultimate solution for managing aquatic vegetation in Minecraft servers. Clear seaweed, kelp, and sea grass with surgical precision while maintaining optimal server performance.

## ✨ Features

- **Smart Clearing** - Remove 5+ types of aquatic plants
- **Multi-World Support** - Works across all loaded worlds
- **Radius Cleaning** - Clear vegetation around players
- **Performance-Friendly** - Chunk-by-chunk processing
- **Real-Time Tracking** - Progress HUD and console logging
- **Multi-Language** - Built-in EN/RU localization
- **Modern API** - Full compatibility with Spigot/Paper 1.13+

## 🛠 Installation

1. Download the latest `.jar` from [Releases](https://github.com/yourname/SeaweedClear/releases)
2. Place in your `plugins/` folder
3. Restart your server
4. (Optional) Edit `plugins/SeaweedClear/config.yml`

## 📋 Commands

| Command | Description | Permission |
|---------|-------------|------------|
| `/sc world <world>` | Clear specific world | `seaweedclear.world` |
| `/sc all` | Clear all loaded worlds | `seaweedclear.all` |
| `/sc radius <size>` | Clear around player | `seaweedclear.radius` |
| `/sc info` | Show progress | `seaweedclear.info` |
| `/sc reload` | Reload config | `seaweedclear.reload` |
| `/sc stop` | Stop active cleanings | `seaweedclear.stop` |

## ⚙ Configuration

```yaml
# plugins/SeaweedClear/config.yml
language: en # en/ru
logging:
  enable: true
performance:
  chunks-per-tick: 2 # Chunks processed per tick
  tick-delay: 5 # Processing interval
```

## 🌍 Localization

Edit these files to add translations:
- `messages_en.yml` (English)
- `messages_ru.yml` (Russian)

## 📜 Permissions

```yaml
seaweedclear.world:
  description: Allows using /sc world
  default: op

seaweedclear.all:
  description: Allows using /sc all
  default: op
  
# ... (all other permissions follow same pattern)
```

## 💻 Developers

Hook into our API:
```java
SeaweedClearAPI api = (SeaweedClearAPI) Bukkit.getPluginManager().getPlugin("SeaweedClear");
api.startCleaning(world, radius, callback);
```

## 📦 Dependencies

- Spigot/Paper 1.13+
- Java 8+

## 🚀 Planned Features

- [ ] Biome-specific clearing
- [ ] Undo functionality
- [ ] Schematic saving

## 📄 License

MIT License - See [LICENSE](LICENSE) for details.
