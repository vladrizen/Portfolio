# Minecraft Server

> **Modded Minecraft server with custom plugins and Docker deployment**

[← Back to Portfolio](../../README.md)

---

## 📖 Overview

A production modded Minecraft server featuring custom plugins, automated backups, and Docker-based deployment for easy scaling and maintenance.

**Status:** ✅ Production

---

## 🎯 My Role

**Server Administrator & Plugin Developer**

- Designed server architecture and modpack configuration
- Developed custom plugins for gameplay enhancement
- Implemented automated backup and recovery systems
- Configured monitoring and player management tools

---

## 🏗️ Architecture

```
┌─────────────────────────────────────────────────────┐
│              Docker Container                        │
│  ┌───────────────────────────────────────────────┐  │
│  │           Minecraft Server (Spigot)           │  │
│  │                                               │  │
│  │  ┌──────────┐  ┌──────────┐  ┌──────────┐   │  │
│  │  │  Custom  │  │  Custom  │  │  Custom  │   │  │
│  │  │ Plugin 1 │  │ Plugin 2 │  │ Plugin 3 │   │  │
│  │  └──────────┘  └──────────┘  └──────────┘   │  │
│  │                                               │  │
│  │  ┌─────────────────────────────────────────┐  │
│  │  │           Modpack (50+ mods)            │  │
│  │  └─────────────────────────────────────────┘  │
│  └───────────────────────────────────────────────┘  │
└─────────────────────────────────────────────────────┘
         │
         ▼
┌─────────────────┐
│   PostgreSQL    │
│   (Player Data) │
└─────────────────┘
```

---

## 🔧 Tech Stack

### Server
- **Platform:** Spigot 1.20.x
- **Runtime:** Java 17
- **Deployment:** Docker Compose
- **Reverse Proxy:** Nginx (for web interface)

### Plugins (Custom)
- **Economy System:** Custom economy with PostgreSQL backend
- **Teleportation:** Waypoint system with cooldowns
- **Protection:** Land claiming and grief prevention

### Mods (50+)
- **Technology:** Mekanism, Thermal Series, Applied Energistics 2
- **Magic:** Botania, Thaumcraft, Blood Magic
- **Exploration:** Biomes O' Plenty, Twilight Forest
- **Quality of Life:** JEI, JourneyMap, AppleSkin

### Infrastructure
- **Database:** PostgreSQL (player data, economy)
- **Backups:** Automated daily snapshots
- **Monitoring:** Custom dashboard for server metrics

---

## 🚀 Features

### Gameplay
- ✅ Custom economy with player shops
- ✅ Waypoint teleportation system
- ✅ Land claiming and protection
- ✅ Custom crafting recipes
- ✅ Balanced mod progression

### Administration
- ✅ Automated daily backups (retained 7 days)
- ✅ Player whitelist management
- ✅ Real-time monitoring dashboard
- ✅ Automated restarts (4 AM daily)
- ✅ Crash detection and auto-recovery

### Performance
- ✅ Pre-generated chunks (reduces lag)
- ✅ Optimized view distance
- ✅ Entity limiting in high-traffic areas
- ✅ Lag monitoring and alerts

---

## 📊 Performance

| Metric | Value |
|--------|-------|
| Max Players | [REDACTED] |
| Average TPS | 19.8/20 |
| Average MSPT | 45ms |
| World Size | [REDACTED] GB |
| Uptime | 99.5% |

---

## 🔐 Security

### Access Control
- **Whitelist:** Only approved players
- **Authentication:** Microsoft account required
- **IP Filtering:** Geo-blocking for high-risk regions

### Server Security
- **Plugin Validation:** All plugins scanned before deployment
- **Network Isolation:** Docker network segmentation
- **DDoS Protection:** [REDACTED]

### Data Protection
- **Backups:** Daily automated backups
- **Database:** Encrypted connections
- **Player Data:** GDPR-compliant retention policy

---

## 📁 Project Structure

```
minecraft-server/
├── docker-compose.yml      # Container orchestration
├── Dockerfile              # Server build
├── plugins/
│   ├── economy/           # Custom economy plugin
│   ├── teleport/          # Waypoint system
│   └── protection/        # Land claiming
├── config/
│   ├── server.properties
│   ├── spigot.yml
│   └── modpack.json
├── scripts/
│   ├── backup.sh          # Automated backups
│   ├── restart.sh         # Graceful restarts
│   └── monitor.sh         # Health checks
└── world/                 # World data (gitignored)
```

---

## 🧪 Backup Strategy

### Automated Backups
- **Frequency:** Daily at 4 AM
- **Retention:** 7 days
- **Storage:** [REDACTED]
- **Verification:** Weekly restore tests

### Backup Contents
- World data (overworld, nether, end)
- Player data and inventories
- Plugin configurations
- Server properties

---

## 📝 Lessons Learned

1. **Pre-generation:** Essential for modded servers with exploration mods
2. **Entity Limiting:** Prevents lag from automated farms
3. **Backup Testing:** Regular restore tests catch issues early
4. **Player Communication:** Discord integration reduces support tickets
5. **Mod Balance:** Careful mod selection prevents progression skips

---

## 🔮 Future Enhancements

- [ ] Custom launcher for modpack distribution
- [ ] Web-based player dashboard
- [ ] Cross-server teleportation
- [ ] Custom boss fights and dungeons
- [ ] Economy integration with Discord bot

---

*Last updated: April 2026*
