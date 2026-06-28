IRIS AI Assistant
=================

Multi-modal AI assistant with natural language interface via Telegram.

Status: Production

Overview
--------
IRIS is an intelligent AI assistant that provides natural language interaction
through Telegram, with support for multiple AI models and contextual
conversations. Features session memory, model fallback, and rate limiting.

My Role: Primary Architect & Developer

Architecture
------------
- Bot Interface: Telegram Bot API
- Core Logic: Python 3.11
- LLM Backend: Ollama (qwen3.5:397b-cloud, mistral:latest)
- Memory: JSON/SQLite session persistence
- Deployment: Docker container

Key Features
------------
- Multi-model support with automatic fallback
- Context-aware conversations (up to 128K tokens)
- Session memory across conversations
- Telegram-native features (replies, formatting, files)
- Rate limiting and abuse prevention
- User allowlist for access control

Performance
-----------
- Average Response Time: 3-8 seconds
- Context Window: 128K tokens
- Uptime: 99.8%

Last updated: June 2026
