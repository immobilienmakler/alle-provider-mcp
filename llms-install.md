# Cline installation and verification guide

This file intentionally avoids inventing a network endpoint or authentication scheme.

## Prerequisites to verify

- Identify the live MCP protocol endpoint and supported transport (Streamable HTTP, SSE, or another documented method).
- Verify TLS, authorization requirements, and whether access is read-only or includes mutations.
- Confirm that the server actually responds to MCP client initialization and tool discovery.
- Confirm the exact configuration format for the intended Cline release.

## Setup procedure

1. Open https://www.alle-provider.de/mcp-schnittstelle/.
2. Locate the **MCP transport URL**, not the page address.
3. Configure the endpoint in Cline using its supported remote MCP server mechanism. If the service requires credentials, use Cline's secure configuration and do not commit them here.
4. Connect and verify MCP initialization, capability negotiation, and the list of tools.
5. Execute a harmless, read-only search with a limited result set.
6. Record tested Cline version, test date, transport, and result in this repository.
7. Only after a successful repeatable test, add a real copy-and-paste setup snippet to README.md.

## Acceptance checklist

- [ ] Actual endpoint and transport documented
- [ ] Authentication / authorization documented
- [ ] Successful setup from README.md or this guide independently observed
- [ ] Read-only operation smoke test passed
- [ ] Timeouts, rate limits and error handling checked
- [ ] 400x400 PNG repository icon available for Cline submission

The checklist is intentionally unchecked until evidence is available.
