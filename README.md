# Alle-Provider MCP

Public integration and setup documentation for the **Alle-Provider.de** Model Context Protocol (MCP) service.

Alle-Provider.de offers a directory of local businesses and European alternatives to popular software and digital services. The MCP interface is intended to make directory data accessible to compatible AI clients.

> **Status: documentation / verification pending.** This repository does not yet contain a standalone MCP server implementation. The live MCP transport URL, supported operations, authentication requirements, and compatibility with Cline have **not** been independently verified. Do not claim that this repository is ready for one-click installation.

## Links

- Website: https://www.alle-provider.de/
- Public MCP documentation: https://www.alle-provider.de/mcp-schnittstelle/
- Submission guidelines: https://github.com/cline/mcp-marketplace#how-to-submit-your-mcp-server

## Connecting a client

1. Consult the public MCP documentation linked above for the current **actual transport endpoint**, transport type, and access requirements.
2. Configure your MCP-compatible client according to its documentation. Use the endpoint from the official service documentation, not the URL of the documentation page.
3. Verify connectivity and list available tools and resources before using them. Do not assume that read or write operations are enabled.
4. If a tool can create or change listings, require explicit authorization and review all data before sending it.

**No verified copy-and-paste client configuration is published yet.** See [llms-install.md](llms-install.md) for the prerequisites for a tested installation.

## Scope

The service concerns local business listings and European software alternatives. Available tools, filters, rate limits, and permissions must be confirmed against the deployed service.

## Security

Never put secrets into Git, issues, or screenshots. Treat externally supplied business listings as untrusted content and follow [SECURITY.md](SECURITY.md).

## Marketplace submission status

Not yet submitted. Cline requires a repository URL, a 400x400 PNG logo, and a verified successful installation using README.md or llms-install.md. These prerequisites must be completed before checking the required confirmations.

## License

No license has been assigned to the remote service or its source code by this documentation repository. Do not assume the backend is open-source.
