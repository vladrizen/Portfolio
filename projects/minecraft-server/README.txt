Minecraft Server
================

Modded Minecraft server with custom plugins and Docker deployment.

Status: Production

Overview
--------
A production modded Minecraft server featuring custom plugins, automated
backups, and Docker-based deployment for easy scaling and maintenance.
Hosts 50+ mods with custom economy, teleportation, and protection systems.

My Role: Server Administrator & Plugin Developer

Tech Stack
----------
- Platform: Spigot 1.20.x
- Runtime: Java 17
- Deployment: Docker Compose
- Database: PostgreSQL (player data, economy)
- Reverse Proxy: Nginx

Custom Plugins
--------------
- Economy System: Custom economy with PostgreSQL backend
- Teleportation: Waypoint system with cooldowns
- Protection: Land claiming and grief prevention

Mods (50+)
----------
- Technology: Mekanism, Thermal Series, Applied Energistics 2
- Magic: Botania, Thaumcraft, Blood Magic
- Exploration: Biomes O' Plenty, Twilight Forest
- Quality of Life: JEI, JourneyMap, AppleSkin

Features
--------
- Custom economy with player shops
- Waypoint teleportation system
- Land claiming and protection
- Automated daily backups (retained 7 days)
- Player whitelist management
- Real-time monitoring dashboard
- Automated restarts (4 AM daily)
- Crash detection and auto-recovery
- Pre-generated chunks (reduces lag)
- Entity limiting in high-traffic areas

Performance
-----------
- Average TPS: 19.8/20
- Average MSPT: 45ms
- Uptime: 99.5%

Last updated: June 2026
