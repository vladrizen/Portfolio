# Homelab Infrastructure

> **Production-grade homelab with comprehensive monitoring and security**

[← Back to Portfolio](../../README.md)

---

## 📖 Overview

A production-grade homelab infrastructure hosting 10+ containerized services with automated monitoring, security hardening, and high availability.

**Status:** ✅ Production

---

## 🎯 My Role

**Infrastructure Architect & Administrator**

- Designed network topology and VLAN segmentation
- Implemented security hardening (UFW, SSH, CVE management)
- Configured monitoring and alerting systems
- Automated deployments and backups

---

## 🏗️ Architecture

```
                    ┌─────────────────┐
                    │   Internet      │
                    └────────┬────────┘
                             │
                    ┌────────▼────────┐
                    │   Firewall      │
                    │   (UFW)         │
                    └────────┬────────┘
                             │
        ┌────────────────────┼────────────────────┐
        │                    │                    │
┌───────▼───────┐   ┌───────▼───────┐   ┌───────▼───────┐
│  Ollama VM    │   │  Services VM  │   │  Web VM       │
│  10.27.27.150 │   │  10.27.27.191 │   │  10.27.27.190 │
│  - LLMs       │   │  - Docker     │   │  - Astro      │
│  - OpenClaw   │   │  - Monitoring │   │  - Tailwind   │
└───────────────┘   └───────────────┘   └───────────────┘
```

### Network Segmentation

| VLAN | Subnet | Purpose |
|------|--------|---------|
| **Management** | 10.27.27.0/24 | Admin access, SSH |
| **Services** | 10.27.27.128/25 | Containerized services |
| **DMZ** | [REDACTED] | Public-facing services |

---

## 🔧 Tech Stack

### Infrastructure
- **Hypervisor:** Proxmox VE
- **Networking:** UFW Firewall, VLANs
- **Remote Access:** Tailscale (zero-trust network)

### Containerization
- **Runtime:** Docker + Docker Compose
- **Orchestration:** Manual (scaling to Kubernetes)
- **Reverse Proxy:** Nginx

### Monitoring
- **Metrics:** [Custom dashboard on port 8081]
- **Logs:** Centralized logging
- **Alerts:** Telegram notifications

### Security
- **Firewall:** UFW with strict rules
- **SSH:** Key-based auth, no passwords
- **CVE Management:** Automated scanning (every 4 hours)
- **Access Control:** Role-based permissions

---

## 🚀 Services Deployed

| Service | Port | Purpose |
|---------|------|---------|
| OpenClaw Gateway | 18789 | AI agent orchestration |
| Briefing Dashboard | 8081 | Daily news + metrics |
| Security Dashboard | [REMOVED] | Security monitoring |
| Ollama API | 11434 | LLM inference |
| [REDACTED] | [REDACTED] | [REDACTED] |

---

## 📊 Performance

| Metric | Value |
|--------|-------|
| Total Services | 10+ |
| Uptime | 99.9% |
| Security Audits | Every 4 hours |
| Critical CVEs | 0 (patched within 24h) |

---

## 🔐 Security Measures

### Implemented
- ✅ UFW firewall with default-deny policy
- ✅ SSH key-based authentication only
- ✅ Regular security audits (automated)
- ✅ CVE scanning and patching
- ✅ Network segmentation (VLANs)
- ✅ Tailscale for remote access (zero-trust)

### In Progress
- 🔄 Fail2ban installation
- 🔄 Intrusion detection system (IDS)
- 🔄 Automated backup verification

---

## 📁 Infrastructure as Code

```
homelab/
├── proxmox/
│   ├── vm-templates/
│   └── lxc-configs/
├── docker/
│   ├── docker-compose.yml
│   └── services/
├── ansible/
│   ├── playbooks/
│   └── roles/
├── monitoring/
│   └── dashboards/
└── security/
    ├── ufw-rules.sh
    └── audit-scripts/
```

---

## 🧪 Disaster Recovery

- **Backups:** Daily snapshots of critical VMs
- **Documentation:** All configs version-controlled
- **Recovery Time Objective:** < 4 hours
- **Recovery Point Objective:** < 24 hours

---

## 📝 Lessons Learned

1. **Network Segmentation:** Critical for containing breaches
2. **Automated Audits:** Catch issues before they become problems
3. **Documentation:** Essential for troubleshooting at 3 AM
4. **Zero-Trust:** Tailscale eliminated need for port forwarding

---

*Last updated: April 2026*
