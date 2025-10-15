# TekUp AI Assistant - Scripts

## MCP Web Scraper

### Filer
- `mcp_web_scraper.py` - MCP-server til web-scraping med Playwright
- `test_mcp_scraper.py` - Test script til at verificere MCP-serveren virker

### Installation
Alle nødvendige pakker er allerede installeret:
- ✅ Python 3.13.7
- ✅ mcp
- ✅ playwright
- ✅ requests
- ✅ beautifulsoup4

### Test MCP-serveren
For at teste om MCP-serveren virker korrekt:

```powershell
python scripts/test_mcp_scraper.py
```

Dette vil:
1. Hente en test-URL
2. Vise resultatet
3. Bekræfte at Playwright fungerer

### Brug i Cursor
Se `configs/claude-desktop/CURSOR_MCP_SETUP.md` for instruktioner om hvordan du tilføjer MCP-serveren i Cursor IDE.

### Værktøjer
Når MCP-serveren er konfigureret, har AI-assistenten adgang til:

#### `fetch_url`
Henter webindhold vha. Playwright (kan håndtere JavaScript)

**Parametre:**
- `url` (påkrævet): URL'en der skal hentes
- `wait_for` (valgfri): CSS selector at vente på

**Eksempel:**
```json
{
  "url": "https://claude.ai/share/ae42cf6f-0409-4ff7-a1c1-1d78e3fb0d6a",
  "wait_for": ".conversation-content"
}
```

#### `fetch_url_simple`
Henter webindhold vha. HTTP requests (hurtigere, men kan ikke håndtere JavaScript)

**Parametre:**
- `url` (påkrævet): URL'en der skal hentes

**Eksempel:**
```json
{
  "url": "https://example.com"
}
```

### Fejlfinding

#### MCP-serveren starter ikke
1. Kontroller Python-installationen: `python --version`
2. Kontroller at alle pakker er installeret: `pip list | findstr mcp`
3. Test scriptet direkte: `python scripts/mcp_web_scraper.py`

#### Playwright fejler
1. Bekræft Chromium er installeret: `python -m playwright install chromium`
2. Test Playwright: `python scripts/test_mcp_scraper.py`

#### Timeout fejl
- Øg timeout i `mcp_web_scraper.py` (standard er 30 sekunder)
- Nogle sider kræver længere tid til at loade dynamisk indhold

