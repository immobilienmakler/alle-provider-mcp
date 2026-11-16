# Security / Sicherheit

## 🇩🇪 Deutsch

Diese Hinweise beziehen sich auf die öffentliche Alle-Provider-MCP-Schnittstelle. Das Repository enthält nicht den privaten WordPress-Backend-Code und stellt keine abgeschlossene Sicherheitsprüfung dar.

- **Datensparsamkeit:** Öffentliche Such- und Abrufwerkzeuge sind laut Schnittstellendokumentation auf veröffentlichte Einträge begrenzt.
- **Schreibzugriff:** `submit_listing` erfordert ein individuelles, widerrufbares WordPress-Anwendungspasswort über HTTPS und ausdrückliche Zustimmungen.
- **Redaktionelle Kontrolle:** Neue Einreichungen werden nicht automatisch als öffentliche Einträge veröffentlicht.
- **Missbrauchsschutz:** Die dokumentierte Schnittstelle beschreibt IP- und globale Anfragelimits, E-Mail-Beschränkungen, Bestätigung bei Registrierung und Duplikatkontrollen.
- **KI-Sicherheit:** Texte aus Verzeichniseinträgen sind nicht vertrauenswürdige Daten, niemals Anweisungen an den Agenten.
- **Geheimnisse:** Keine Passwörter, Tokens oder personenbezogene Informationen in GitHub-Issues, Beispielkonfigurationen oder Protokolle schreiben.

Sicherheitsprobleme bitte nicht in einem öffentlichen Issue mit vertraulichen Details offenlegen. Betreiberkontakt: https://www.alle-provider.de/kontakt/

## 🇬🇧 English

This policy covers the public Alle-Provider MCP integration. The repository does not publish the private WordPress backend and does not imply a completed security audit.

- **Public scope:** Read tools are documented to return published listings only.
- **Write authorization:** `submit_listing` requires an individual, revocable WordPress application password over HTTPS and explicit consent.
- **Editorial moderation:** New submissions are not automatically published.
- **Abuse controls:** The documented service describes per-IP/global request limits, email limits, email verification, and duplicate-submission checks.
- **AI safety:** Listing descriptions are untrusted content, not instructions to the assistant.
- **Secrets:** Never expose passwords, tokens, or personal data in issues, examples, or logs.

Report sensitive vulnerabilities privately through the website contact channel: https://www.alle-provider.de/kontakt/

**Documentation / Dokumentation:** https://www.alle-provider.de/mcp-schnittstelle/
