# MCP client setup / MCP-Client-Einrichtung

## 🇩🇪 Deutsch

Der **öffentliche Alle-Provider-MCP-Server** ist ein Remote-Endpunkt. Für die Nutzung seiner veröffentlichten Verzeichnisdaten muss kein WordPress-Server lokal installiert werden.

- **Endpunkt:** `https://www.alle-provider.de/wp-json/alle-provider-mcp/v1/mcp`
- **Transport laut Betreiber-Dokumentation:** HTTPS, JSON-RPC 2.0 per POST
- **Dokumentierte Protokollversion:** `2025-06-18`
- **Unterstützte Methoden:** `initialize`, `ping`, `tools/list`, `tools/call`

### Erste Verbindung testen

```bash
curl -X POST 'https://www.alle-provider.de/wp-json/alle-provider-mcp/v1/mcp' \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -H 'MCP-Protocol-Version: 2025-06-18' \
  --data '{"jsonrpc":"2.0","id":1,"method":"initialize","params":{"protocolVersion":"2025-06-18","capabilities":{},"clientInfo":{"name":"alle-provider-test","version":"1.0"}}}'
```

Weitere Werkzeuge abrufen:

```bash
curl -X POST 'https://www.alle-provider.de/wp-json/alle-provider-mcp/v1/mcp' \
  -H 'Content-Type: application/json' \
  --data '{"jsonrpc":"2.0","id":2,"method":"tools/list","params":{}}'
```

**Cline:** Trage die obige Endpunktadresse nur in einer Cline-Version ein, die den dokumentierten Remote-HTTP-MCP-Transport unterstützt. Prüfe beim Verbindungsaufbau `initialize` und `tools/list`. Ein Cline-Ein-Klick-Setup wurde noch nicht nachgewiesen; daher wird keine unbestätigte JSON-Konfiguration als garantiert funktionierend ausgegeben.

Die Werkzeuge `find_terms`, `search_listings` und `get_listing` sind öffentlich dokumentiert. `register_account` erfordert Datenschutz-Zustimmung und versendet einen Bestätigungslink. `submit_listing` benötigt eine persönliche WordPress-Anwendungspasswort-Authentifizierung und ausdrückliche Zustimmungen; Einreichungen werden moderiert.

## 🇬🇧 English

The public Alle-Provider MCP service is a **remote endpoint**. No local WordPress installation is needed to browse published directory data.

- **Endpoint:** `https://www.alle-provider.de/wp-json/alle-provider-mcp/v1/mcp`
- **Documented transport:** HTTPS, JSON-RPC 2.0 over POST
- **Documented protocol version:** `2025-06-18`
- **Methods:** `initialize`, `ping`, `tools/list`, `tools/call`

Run the initialization and tools/list examples above to verify protocol interoperability. In Cline, configure the URL only if your client version supports this remote MCP transport. No verified one-click Cline installation is claimed.

The public tools are `find_terms`, `search_listings`, and `get_listing`. Account registration requires privacy consent and email confirmation. Submitting a listing requires an individual WordPress application password, explicit consent, and editorial review.

**Source of interface details / Quelle:** https://www.alle-provider.de/mcp-schnittstelle/
