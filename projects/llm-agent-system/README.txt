LLM Agent System
================

Multi-agent AI orchestration platform using Hermes Agent framework.

Status: Production

Overview
--------
A production multi-agent AI system featuring 3 specialized agents (Jasmine,
Lily, Jerry) with cross-agent communication, automated scheduling, real-time
dashboards, and persistent memory across sessions. The system handles personal
operations, business automation, and IT infrastructure coordination.

My Role: System Architect & Lead Developer

Architecture
------------
- Framework: Hermes Agent (by Nous Research)
- Runtime: Node.js 22.x
- Language: TypeScript
- Messaging: Telegram Bot API (3 bot accounts)
- LLM Backend: Ollama (internal VM) + cloud model providers
- Automation: Cron-based scheduling (4 agent + 3 no_agent jobs)
- Dashboard: React + Python with SVG sparklines

Agent Personas
--------------
- Jasmine (Main): Executive assistant, personal operations, technical
  coordination. Calm, organized, proactive. Runs on deepseek-v4-flash.
- Lily (Business): Marketing, content operations, social media, SEO.
  Business-optimized model.
- Jerry (IT): Infrastructure operations, system administration.

Automation (7 Cron Jobs)
------------------------
- Kanban Triage (hourly) - Task prioritization
- Homelab Dashboard (every 6h) - Infrastructure metrics
- Network Discovery (every 12h) - ARP scan + topology
- News Briefing (7am daily) - AI news aggregation
- Health Check (no_agent) - Service availability
- Hermes Update (no_agent) - Platform updates
- TrueNAS App Check (no_agent) - App status verification

Security Features
-----------------
- Telegram allowlist (authorized users only)
- Exec approvals with command allowlist
- Bot tokens stored in config (encrypted at rest)
- Separate workspaces per agent
- Role-based tool access
- Security audits every 4 hours
- CVE scanning on all hosts
- Automated alerting via Telegram

Key Capabilities
----------------
- Cross-agent communication (Jasmine <-> Lily <-> Jerry)
- Specialized sub-agents (Lily has 3: research, social, analytics)
- Context sharing between agents
- Memory persistence across sessions
- Session search across conversation history
- Skill-based procedural memory
- Cron job management with delivery routing
- Background task delegation

Recent Work
-----------
- Migrated from OpenClaw to Hermes Agent framework
- Implemented persistent memory system (user profile + agent notes)
- Built session search across conversation history
- Created skill management system (create, patch, delete)
- Set up cron job infrastructure with no_agent mode
- Integrated Telegram delivery for scheduled tasks
- Added background process management
- Implemented Kanban task orchestration
- Built self-improving agent loop skill

Last updated: June 2026
