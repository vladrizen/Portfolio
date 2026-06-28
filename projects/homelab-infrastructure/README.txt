Homelab Infrastructure
======================

Production-grade homelab with comprehensive monitoring, security, and automation.

Status: Production (99.9% uptime)

Overview
--------
A production-grade homelab infrastructure hosting 10+ containerized services
with automated monitoring, security hardening, and high availability. The
infrastructure spans 9 fleet hosts managed via SSH, with centralized logging,
intrusion detection, and threat intelligence.

My Role: Infrastructure Architect & Administrator

Tech Stack
----------
- Hypervisor: Proxmox VE (10+ VMs)
- Container Runtime: Docker + Docker Compose
- Networking: UFW Firewall, VLANs, Tailscale (zero-trust)
- Reverse Proxy: Nginx with CA-signed certificates
- Storage: TrueNAS SCALE (ZFS, 10GbE)
- Remote Access: Tailscale mesh network

Security Stack
--------------
- UFW firewall with default-deny policy on all hosts
- SSH key-based authentication only (no passwords)
- Suricata IDS (7.0.3) with ET Open ruleset on dedicated sensor
- CrowdSec threat intelligence (LAPI + nftables bouncer)
- Lynis security audits across all fleet hosts (every 4 hours)
- rkhunter + chkrootkit malware scanning (daily)
- Automated CVE scanning and patching
- Network segmentation (VLANs)

Monitoring & Observability
--------------------------
- Custom React+Python dashboard with per-host health indicators
- TrendStore metrics persistence (54+ metrics per collection cycle)
- SVG sparkline trend visualization
- Suricata alert digest (daily Telegram report)
- CrowdSec threat dashboard
- Jellyfin media server monitoring (272 movies, 149 series)
- ZFS snapshot health tracking (hourly/daily/weekly rotation)

Key Services Deployed
--------------------
- Hermes Agent (AI orchestration, 4 cron jobs)
- Ollama LLM inference (qwen3.6:27b, multiple models)
- OpenWebUI (LLM chat interface)
- Jellyfin Media Server (Vault 49)
- Portainer (container management)
- Uptime Kuma (service monitoring)
- TrueNAS SCALE (NAS with Wasabi off-site backup)
- Custom Briefing Dashboard
- Homelab Infrastructure Dashboard

Backup & Disaster Recovery
--------------------------
- Proxmox VM snapshots: hourly (24h), daily (7d), weekly (4wk)
- TrueNAS ZFS snapshots with tiered retention
- Key data synced to Wasabi (off-site)
- Recovery Time Objective: < 4 hours
- Recovery Point Objective: < 24 hours

Recent Work
-----------
- Deployed Homelab Root CA with CA-signed certs across all services
- Migrated all HTTP services to HTTPS (port 443)
- Integrated TrendStore metrics persistence into dashboard
- Fixed ram_collector watchdog (WATCHDOG_USEC, post-collection ping)
- Standardized SSH password auth across fleet for local access
- Deployed Suricata IDS with threshold.conf suppression rules
- Set up CrowdSec LAPI with syslog ingestion (8 hosts)
- Automated fleet-wide Lynis audits (parallel, 12h + 4am)
- Automated fleet-wide malware scans (daily, silent-clean)
- Created jasmine user with passwordless sudo on all hosts

Last updated: June 2026
