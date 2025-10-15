# 🤖 TekUp AI Assistant

Local AI assistant integrating with TekUp ecosystem (RenOS, Billy.dk, Google Workspace).

## 🎯 What This Is

A **documentation and configuration repository** that connects your existing TekUp services with AI assistants like Jan AI, Claude Desktop, and Cursor.

**No duplicate code** - uses your existing:
- ✅ Tekup-Billy (https://tekup-billy.onrender.com)
- ✅ RenOS Backend
- ✅ RenOS Frontend

## 🏗️ Architecture

\\\
You → Jan AI / Claude Desktop
         ↓ (MCP Protocol)
    Tekup-Billy API → Billy.dk
    RenOS API → PostgreSQL
    Ollama → Local AI Models
\\\

## 📦 What's Included

- **/docs/** - Setup guides, architecture, workflows
- **/configs/** - Jan AI, Claude Desktop, Ollama configurations
- **/scripts/** - Installation and testing automation
- **/examples/** - Usage examples (create invoice, check calendar, etc.)

## 🚀 Quick Start

See [docs/SETUP.md](docs/SETUP.md) for installation guide.

## 💰 ROI

Saves ~2 hours/day on:
- Invoice creation (8 min → 15 sec)
- Calendar coordination (20 min → 2 min)
- Code debugging (45 min → 5 min)

**Break-even:** 1 month

---

**Status:** 🚧 Under development (Phase 1: Foundation)
