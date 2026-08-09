# Security & Privacy

CERVAULT separates the local control runtime, customer-facing surfaces, confidential implementation, and secret material. Public documentation describes behavior and boundaries without exposing proprietary runtime internals.

## Local runtime

The Windows runtime operates as a local background service with a tray/desktop control surface. The browser UI is optional diagnostics and is not required for normal startup.

Local runtime status, non-secret settings, client coverage, and governed-run evidence do not require a model-provider credential.

## Credentials

CERVAULT does not own production identity credentials, payment credentials, or model-provider credentials. Provider credentials remain host-owned and are not collected by the first-run surface.

Do not put API keys, passwords, signing keys, payment credentials, or raw secrets in task prompts, repository files, connector requests, or evidence records.

## Repository safety

CERVAULT resolves governed repository work through declared scope. Unknown or overlapping repository scope is rejected rather than guessed.

The current policy denies main/master mutation, force push, free-form shell command text, raw-secret execution paths, direct connector execution outside a persisted run, and runless role execution.

## Side-effect authorization

A side effect is not authorized just because an AI requested it. Governed operations pass pre-action checks and policy before a bounded capability is issued. The resulting operation is recorded with a receipt and becomes part of acceptance evidence.

## Software integrity

Install only signed CERVAULT releases from the official download channel. The v5.3 installation lifecycle verifies release hashes and package inventory before activation, installs pinned dependencies, and runs a functional self-test. Failed verification must stop activation or trigger rollback.

## IP boundary

Public/client material and confidential implementation are classified separately. Customer-distributed artifacts must not contain confidential runtime source or tracked secret material.

## Privacy boundary

CERVAULT governance evidence records execution state and control evidence. The data processed by an attached AI client or external model provider is also subject to that client's and provider's own behavior, configuration, and privacy terms. CERVAULT should not be described as making an external provider private by itself.

For legal privacy, retention, and data-processing terms, use the Privacy Policy and Terms published with the commercial release.
