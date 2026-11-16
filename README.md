<div align="center">

# Alle-Provider MCP
### Unternehmens- und Softwareverzeichnisse für KI-Assistenten
### Business & software directories for AI assistants

**Deutsch · English** · **Model Context Protocol** · **HTTPS / JSON-RPC 2.0**

[**Projektwebseite / Project website**](https://immobilienmakler.github.io/alle-provider-mcp/) · [**Offizielle API-Dokumentation / Official API documentation**](https://www.alle-provider.de/mcp-schnittstelle/) · [**Alle-Provider.de**](https://www.alle-provider.de/)

</div>

---

## 🇩🇪 Deutsch

**Alle-Provider MCP** verbindet MCP-kompatible KI-Assistenten mit den öffentlichen Verzeichnissen von [Alle-Provider.de](https://www.alle-provider.de/). Der Server ermöglicht die strukturierte Suche nach lokalen Unternehmen sowie europäischen Software- und Digitaldienst-Alternativen. Registrierungen und die Einreichung neuer Verzeichniseinträge werden über eigene, kontrollierte Werkzeuge abgewickelt.

### Was ist möglich?

| MCP-Werkzeug | Funktion | Zugang |
|---|---|---|
| `find_terms` | Kategorien und Orte finden; passende IDs für Filter erhalten | Öffentlich |
| `search_listings` | Veröffentlichte Einträge durchsuchen und nach Verzeichnis, Kategorie oder Ort filtern (max. 20 je Seite) | Öffentlich |
| `get_listing` | Einen veröffentlichten Eintrag mit ausführlicher Beschreibung aufrufen | Öffentlich |
| `register_account` | Registrierungsprozess mit E-Mail-Bestätigung starten, sofern Registrierung aktiviert ist | Öffentlich, mit Datenschutz-Zustimmung |
| `submit_listing` | Einreichung eines Unternehmens oder Digitaldienstes zur redaktionellen Prüfung | Authentifiziert, mit Zustimmungen |

**Wichtig:** Eine Einreichung ist **keine automatische Veröffentlichung**. Neue Inhalte durchlaufen einen Prüfprozess. Die öffentlichen Lesewerkzeuge liefern nur veröffentlichte Einträge.

### Verbindung

| Eigenschaft | Wert |
|---|---|
| MCP-Endpunkt | `https://www.alle-provider.de/wp-json/alle-provider-mcp/v1/mcp` |
| Transport | HTTPS, JSON-RPC 2.0 via HTTP POST |
| Dokumentierte MCP-Protokollversion | `2025-06-18` |
| Methoden | `initialize`, `ping`, `tools/list`, `tools/call` |

Die genaue Einrichtung hängt davon ab, welche Remote-MCP-Transportarten der jeweilige Client unterstützt. Die dokumentierte API-Adresse ist **nicht** mit der Dokumentations-Webseite zu verwechseln.

```bash
curl -X POST 'https://www.alle-provider.de/wp-json/alle-provider-mcp/v1/mcp' \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -H 'MCP-Protocol-Version: 2025-06-18' \
  --data '{"jsonrpc":"2.0","id":1,"method":"initialize","params":{"protocolVersion":"2025-06-18","capabilities":{},"clientInfo":{"name":"api-demo","version":"1.0"}}}'
```

Weitere Beispiele, Parameter, Berechtigungen und Hinweise findest du unter [Offizielle MCP-Dokumentation](https://www.alle-provider.de/mcp-schnittstelle/) sowie in [llms-install.md](llms-install.md).

### Datenschutz & Berechtigungen

Die öffentlichen Abfragen sind auf veröffentlichte Verzeichnisdaten beschränkt. Für `submit_listing` sind ein separates WordPress-Benutzerkonto und ein widerrufbares Anwendungspasswort via HTTPS Basic Authentication nötig. Bei Registrierung und Einreichung gelten zusätzliche Zustimmungs- und Prüfregeln. Zugangsdaten niemals im Repository hinterlegen.

---

## 🇬🇧 English

**Alle-Provider MCP** connects MCP-compatible AI assistants to the public directories on [Alle-Provider.de](https://www.alle-provider.de/). It exposes structured discovery of local businesses and European software and digital-service alternatives. Separate tools support account registration and moderated directory submissions.

### Available tools

| MCP tool | Purpose | Access |
|---|---|---|
| `find_terms` | Discover categories and locations and obtain filter IDs | Public |
| `search_listings` | Search published listings by directory, category and location (up to 20 per page) | Public |
| `get_listing` | Retrieve detailed information about a published listing | Public |
| `register_account` | Start email-verified account registration when enabled | Public, privacy consent required |
| `submit_listing` | Submit a business or digital service for editorial review | Authenticated, consent required |

Submissions are **not automatically published**. Public read tools only expose published listings.

### Connection details

| Property | Value |
|---|---|
| MCP endpoint | `https://www.alle-provider.de/wp-json/alle-provider-mcp/v1/mcp` |
| Transport | HTTPS, JSON-RPC 2.0 over HTTP POST |
| Documented MCP protocol version | `2025-06-18` |
| Methods | `initialize`, `ping`, `tools/list`, `tools/call` |

Client compatibility depends on its supported remote MCP transport and initialization behavior. The documentation page is **not** the MCP endpoint.

For request examples, arguments and access requirements, see [the official API documentation](https://www.alle-provider.de/mcp-schnittstelle/) and [llms-install.md](llms-install.md).

### Authentication & data handling

Public discovery is limited to published directory records. `submit_listing` requires HTTPS Basic Authentication with an individual, revocable WordPress application password. Registration and submission require appropriate consent; submitted entries undergo editorial review. Never commit credentials.

---

## Repository / Repository-Hinweis

This repository provides public integration documentation and the bilingual GitHub Pages project site. It does not contain the private WordPress backend. A successful installation in a specific Cline version has not been independently verified here.

Dieses Repository enthält die öffentliche Integrationsdokumentation und die zweisprachige GitHub-Pages-Projektseite, nicht den privaten WordPress-Backend-Code. Ein erfolgreicher Installationstest mit einer konkreten Cline-Version ist hier noch nicht unabhängig nachgewiesen.

[Security / Sicherheit](SECURITY.md) · [Installation / Einrichtung](llms-install.md) · [GitHub Pages source / Webseitenquelltext](docs/index.html)
