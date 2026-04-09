# IRIS AI Assistant

> **Multi-modal AI assistant with natural language interface**

[← Back to Portfolio](../../README.md)

---

## 📖 Overview

IRIS is an intelligent AI assistant that provides natural language interaction through Telegram, with support for multiple AI models and contextual conversations.

**Status:** ✅ Production

---

## 🎯 My Role

**Primary Architect & Developer**

- Designed conversation flow and context management
- Implemented Telegram Bot API integration
- Configured Ollama LLM backend with model routing
- Built memory and session persistence layer

---

## 🏗️ Architecture

```
┌─────────────┐     ┌──────────────┐     ┌─────────────┐
│   Telegram  │────▶│  IRIS Core   │────▶│   Ollama    │
│    Bot API  │     │  (Python)    │     │   LLMs      │
└─────────────┘     └──────────────┘     └─────────────┘
                           │
                           ▼
                    ┌──────────────┐
                    │   Session    │
                    │   Memory     │
                    └──────────────┘
```

### Components

| Component | Technology | Purpose |
|-----------|------------|---------|
| **Bot Interface** | Telegram Bot API | User communication |
| **Core Logic** | Python 3.11 | Conversation management |
| **LLM Backend** | Ollama | Model inference |
| **Memory** | JSON/SQLite | Session persistence |

---

## 🔧 Tech Stack

- **Language:** Python 3.11
- **Bot Framework:** python-telegram-bot
- **LLM:** Ollama (qwen3.5:397b-cloud, mistral:latest)
- **Deployment:** Docker container
- **Monitoring:** Custom health checks

---

## 🚀 Key Features

- ✅ Multi-model support with automatic fallback
- ✅ Context-aware conversations (up to 128K tokens)
- ✅ Session memory across conversations
- ✅ Telegram-native features (replies, formatting, files)
- ✅ Rate limiting and abuse prevention

---

## 📊 Performance

| Metric | Value |
|--------|-------|
| Average Response Time | 3-8 seconds |
| Context Window | 128K tokens |
| Daily Active Users | [REDACTED] |
| Uptime | 99.8% |

---

## 🔐 Security

- Bot token stored in environment variables
- User allowlist for access control
- Input sanitization and validation
- Rate limiting per user

---

## 📁 Project Structure

```
iris-ai-assistant/
├── bot.py                 # Main bot logic
├── conversation.py        # Context management
├── models.py             # LLM routing
├── memory.py             # Session persistence
├── config.py             # Configuration
├── requirements.txt      # Dependencies
└── Dockerfile            # Container build
```

---

## 🧪 Testing

- Unit tests for conversation logic
- Integration tests with Telegram API
- Load testing for rate limiting

---

## 📝 Lessons Learned

1. **Context Management:** Implemented sliding window for long conversations
2. **Model Fallback:** Added automatic retry with alternate models
3. **User Experience:** Telegram formatting significantly improves readability

---

*Last updated: April 2026*
