# Security Policy

CERVAULT is an AI agent governance harness. Security reports should not be filed as public issues when they contain exploitable details, credentials, customer data, or private logs.

## Reporting a vulnerability

Use the private support channel listed at https://cervault.marsci-diagnostics.com/support/ and include only the minimum information required to reproduce the issue.

Please include:
- affected CERVAULT version and platform,
- a concise description of the impact,
- reproducible steps using sanitized data,
- relevant logs with secrets and customer information removed.

Do not include API keys, access tokens, private repository content, billing identifiers, customer data, or production credentials in GitHub Issues.

## Public preview posture

The current `v5.3.0-wave-d-preview.1` release is a public preview. Preview binaries are unsigned unless an individual release asset explicitly states otherwise. Verify downloaded artifacts against the published `SHA256SUMS.txt` before use.

## Scope

Public security reporting covers the distributed CERVAULT client, public release artifacts, documented interfaces, and the public website. Internal control-plane implementation details and private source are intentionally not distributed through this repository.
