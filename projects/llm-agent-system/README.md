# LLM Agent System

> **Multi-agent orchestration platform using OpenClaw framework**

[← Back to Portfolio](../../README.md)

---

## 📖 Overview

A production multi-agent AI system built on OpenClaw, featuring 3 specialized agents (Jasmine, Lily, Jerry) with cross-agent communication, automated scheduling, and real-time dashboards.

**Status:** ✅ Production

---

## 🎯 My Role

**System Architect & Lead Developer**

- Designed agent architecture and communication patterns
- Implemented cross-agent messaging protocol
- Built automated briefing dashboard with live data
- Configured cron-based automation (9 scheduled jobs)
- Developed security hardening and audit systems

---

## 🏗️ Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                     OpenClaw Gateway                         │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  ┌──────────┐    ┌──────────┐    ┌──────────┐              │
│  │ Jasmine  │◀──▶│   Lily   │◀──▶│  Jerry   │              │
│  │ (Main)   │    │(Business)│    │  (IT)    │              │
│  │          │    │          │    │          │              │
│  │ qwen3.5  │    │ glm-5    │    │kimi-k2.5 │              │
│  │ 397B     │    │ cloud    │    │ cloud    │              │
│  └────┬─────┘    └────┬─────┘    └────┬─────┘              │
│       │               │               │                     │
│       └───────────────┼───────────────┘                     │
│                       │                                     │
│              ┌────────▼────────┐                            │
│              │  Telegram Bots  │                            │
│              │  (3 accounts)   │                            │
│              └─────────────────┘                            │
│                                                              │
└─────────────────────────────────────────────────────────────┘
                              │
                              ▼
                    ┌─────────────────┐
                    │   Dashboards    │
                    │   (Port 8081)   │
                    └─────────────────┘
```

---

## 🔧 Tech Stack

### Core Platform
- **Framework:** OpenClaw 2026.4.5
- **Runtime:** Node.js 22.x
- **Language:** TypeScript

### AI Models
| Agent | Model | Parameters | Purpose |
|-------|-------|------------|---------|
| **Jasmine** | qwen3.5:397b-cloud | 397B | Coordination, memory |
| **Lily** | glm-5:cloud | [REDACTED] | Business writing |
| **Jerry** | kimi-k2.5:cloud | [REDACTED] | IT operations |

### Infrastructure
- **LLM Backend:** Ollama (http://10.27.27.150:11434)
- **Messaging:** Telegram Bot API (3 bots)
- **Automation:** OpenClaw Cron (9 jobs)
- **Dashboard:** Astro + Tailwind CSS

---

## 🚀 Features

### Agent Capabilities
- ✅ Cross-agent communication (Jasmine↔Lily↔Jerry)
- ✅ Specialized sub-agents (Lily has 3: research, social, analytics)
- ✅ Context sharing between agents
- ✅ Exec approvals with allowlist
- ✅ Memory persistence across sessions

### Automation (9 Cron Jobs)
| Job | Schedule | Purpose |
|-----|----------|---------|
| AI News Scanner | 3:15 AM daily | Overnight AI news aggregation |
| Nightly Build | 4:00 AM daily | Dashboard improvements |
| Briefing Auto-Refresh | Every 4 hours | Keep dashboard data fresh |
| YouTube Fetch | Every 2 hours | Track 7 tech channels |
| Security Audit | Every 4 hours | CVE scanning |
| Daily Check-in | Every 2 hours | User reminders |
| Memory Maintenance | Sundays 10 AM | Curate long-term memory |
| Weekly Review | Fridays 2 PM | Week retrospective |
| OpenClaw Update | Weekly | Platform updates |

### Dashboard Features
- ✅ Live clock (updates every second)
- ✅ AI News widget (from overnight scans)
- ✅ Nightly Builds widget (changelog)
- ✅ YouTube carousel (9 videos, 7 channels)
- ✅ Hot topics tags
- ✅ Quick links grid
- ✅ Auto-refresh every 4 hours

---

## 📊 Performance

| Metric | Value |
|--------|-------|
| Agents Deployed | 3 (+ 3 sub-agents) |
| Daily Messages | [REDACTED] |
| Cron Jobs | 9 active |
| Dashboard Uptime | 99.9% |
| Average Response Time | 5-15 seconds (cloud models) |

---

## 🔐 Security

### Access Control
- **Telegram Allowlist:** Only authorized users (ID: 8663373707)
- **Exec Approvals:** All commands require approval
- **Bot Tokens:** Stored in config (encrypted at rest)

### Agent Isolation
- Separate workspaces per agent
- Isolated session management
- Role-based tool access

### Monitoring
- Security audits every 4 hours
- CVE scanning on all hosts
- Automated alerting via Telegram

---

## 📁 Project Structure

```
.openclaw/
├── openclaw.json           # Main config (agents, models, channels)
├── exec-approvals.json     # Command allowlist
├── skills/                 # Custom agent skills
│   ├── ai-news-scanner/
│   ├── nightly-build/
│   ├── morning-brief/
│   ├── weekly-review/
│   └── memory-maintenance/
├── workspace/
│   ├── briefing-dashboard/ # Live dashboard (port 8081)
│   ├── research/ai-pulse/  # AI news reports
│   ├── memory/             # Session memory
│   ├── lily/               # Lily's workspace
│   └── jerry/              # Jerry's workspace
└── telegram/               # Bot state & offsets
```

---

## 🧪 Testing & Quality

- Automated security audits (every 4 hours)
- Dashboard health checks (every 5 minutes)
- Model availability monitoring
- Cron job execution tracking

---

## 📝 Lessons Learned

1. **Model Selection:** Cloud models for quality, local for cost savings
2. **Timeout Configuration:** Local models need 2x timeout vs cloud
3. **Agent Communication:** Cross-messaging enables complex workflows
4. **Dashboard Freshness:** Auto-refresh critical for user trust
5. **Memory Management:** Daily logs + curated long-term memory works best

---

## 🔮 Future Enhancements

- [ ] Email integration for Morning Brief
- [ ] Voice interface (ElevenLabs TTS)
- [ ] Additional sub-agents for Lily
- [ ] Historical briefing archive
- [ ] Advanced analytics dashboard

---

*Last updated: April 2026*
