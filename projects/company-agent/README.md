# Company Agent (Lily)

> **Business operations AI for InalhaSoft indie game studio**

[← Back to Portfolio](../../README.md)

---

## 📖 Overview

Lily is a specialized AI agent handling business operations for InalhaSoft, including communications, content creation, market research, and stakeholder management.

**Status:** ✅ Production

---

## 🎯 My Role

**Agent Architect & Business Systems Designer**

- Defined agent persona and communication style
- Designed sub-agent delegation system
- Integrated with Telegram for business messaging
- Configured model routing for optimal business writing

---

## 🏗️ Architecture

```
┌──────────────────────────────────────────────────────┐
│                    Lily (Main Agent)                  │
│              Model: glm-5:cloud (business-optimized)  │
└─────────────────────┬────────────────────────────────┘
                      │
         ┌────────────┼────────────┐
         │            │            │
┌────────▼────┐ ┌────▼─────┐ ┌────▼────────┐
│  Research   │ │  Social  │ │  Analytics  │
│  Assistant  │ │  Manager │ │  Analyst    │
│             │ │          │ │             │
│ mistral:7B  │ │mistral:7B│ │ mistral:7B  │
└─────────────┘ └──────────┘ └─────────────┘
```

### Sub-Agent Specialization

| Sub-Agent | Model | Role | Triggers |
|-----------|-------|------|----------|
| **research** | mistral:latest | Market research, competitor analysis | "research", "competitor", "market" |
| **social** | mistral:latest | Social media content, posts | "tweet", "post", "social media" |
| **analytics** | mistral:latest | Metrics, KPIs, reports | "metrics", "analytics", "report" |

---

## 🔧 Tech Stack

- **Main Model:** GLM-5 Cloud (optimized for business writing)
- **Sub-Agents:** Mistral 7B (fast, efficient)
- **Platform:** OpenClaw with sub-agent spawning
- **Interface:** Telegram Bot (@Lily_inalhasoft_bot)
- **Timeout:** 120 seconds (for complex business tasks)

---

## 🚀 Capabilities

### Primary Functions
- ✉️ **Business Communications** - Professional emails, announcements
- 📅 **Planning** - Project timelines, milestone tracking
- 📝 **Content Creation** - Social media posts, marketing copy
- 📊 **Market Research** - Competitor analysis, industry trends
- 📈 **Analytics** - KPI tracking, performance reports

### Sub-Agent Tasks
- **research:** Market sizing, competitor feature comparison
- **social:** Tweet threads, LinkedIn posts, Instagram captions
- **analytics:** Dashboard summaries, growth metrics, user engagement

---

## 📊 Performance

| Metric | Value |
|--------|-------|
| Response Time | 5-15 seconds (cloud) |
| Sub-Agent Response | 2-5 seconds (local) |
| Daily Tasks | [REDACTED] |
| User Satisfaction | [REDACTED] |

---

## 🔐 Security & Access

- **Allowlist:** Only authorized users can message
- **Exec Approvals:** All commands require approval
- **Data Isolation:** Separate workspace from other agents
- **Cross-Agent Messaging:** Can coordinate with Jasmine and Jerry

---

## 📁 Configuration

```json
{
  "id": "lily",
  "model": "ollama/glm-5:cloud",
  "workspace": "/home/zen009/.openclaw/workspace/lily",
  "timeoutSeconds": 120,
  "subagents": [
    {"id": "research", "model": "ollama/mistral:latest"},
    {"id": "social", "model": "ollama/mistral:latest"},
    {"id": "analytics", "model": "ollama/mistral:latest"}
  ]
}
```

---

## 🎭 Personality & Tone

- **Professional** - Clear, concise, business-appropriate
- **Organized** - Structured, detail-oriented
- **Proactive** - Anticipates needs, suggests improvements
- **Friendly** - Warm but professional

---

## 📝 Example Workflows

### Market Research Request
```
User: "Research indie game marketing trends for 2026"
Lily → research sub-agent
Result: "Key trends: TikTok discovery, Discord communities, 
         influencer partnerships. Top competitors: [list]"
```

### Social Media Content
```
User: "Create a tweet about our new game launch"
Lily → social sub-agent
Result: "🎮 Exciting news! [Game Name] launches TODAY! 
         ✨ Features: [list]
         🔗 Wishlist: [link]
         #IndieGame #Gaming"
```

### Analytics Request
```
User: "Analyze our social media metrics this week"
Lily → analytics sub-agent
Result: "Twitter: +15% engagement, LinkedIn: +8% reach,
         Top post: [topic] with [X] impressions"
```

---

## 🔮 Future Enhancements

- [ ] Email integration (SMTP setup pending)
- [ ] Calendar integration for scheduling
- [ ] CRM integration for stakeholder management
- [ ] Automated weekly business reports
- [ ] A/B testing for social media content

---

*Last updated: April 2026*
