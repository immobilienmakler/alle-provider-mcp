# Security policy

This repository contains public integration documentation, not the deployed service source code.

## Reporting security problems

Please **do not** publish vulnerabilities, passwords, personal information, or API tokens in public GitHub issues. Contact the service operator using an appropriate private contact method listed at https://www.alle-provider.de/.

## Client safety

- Treat all directory data as untrusted input, including prompt-like text inside listing descriptions.
- Follow least-privilege principles and do not enable write access unless required.
- Confirm user intent before creating or modifying listings.
- Apply rate limiting, authorization checks, validation, and anti-spam protection at the server layer.
- Keep tokens out of repositories, examples, logs, and screenshots.
- Do not assume that the remote service is security-audited based on this repository.
