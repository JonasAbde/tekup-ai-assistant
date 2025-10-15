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
  - **MCP_WEB_SCRAPER_GUIDE.md** - Complete guide to web scraping with MCP
- **/configs/** - Jan AI, Claude Desktop, Ollama configurations
  - **claude-desktop/** - MCP configuration and setup instructions
- **/scripts/** - Installation and testing automation
  - **mcp_web_scraper.py** - Python MCP server for web scraping ✅
  - **test_mcp_scraper.py** - Test suite for MCP server ✅
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

## 🆕 Latest: MCP Web Scraper

✅ **Just Implemented!** Python-based MCP server for web scraping

**Features:**
- Fetch dynamic JavaScript-rendered content (using Playwright)
- Access shared Claude conversations directly
- Simple HTTP requests for static pages
- Fully tested and ready to use

**Get Started:**
1. Follow setup guide: [docs/MCP_WEB_SCRAPER_GUIDE.md](docs/MCP_WEB_SCRAPER_GUIDE.md)
2. Test installation: `python scripts/test_mcp_scraper.py`
3. Add to Cursor Settings and restart
4. Start scraping web content with AI assistance!

---

**Status:** 🚧 Under development (Phase 1: Foundation + MCP Web Scraper ✅)
