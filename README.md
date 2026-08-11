# CERVAULT

CERVAULT is a governed execution layer for AI work. This repository is the official public distribution and release surface for CERVAULT.

## Downloads

Verified native binaries are published under GitHub Releases only after the corresponding platform acceptance gate passes. Verified container images are published through GHCR after Docker acceptance passes.

- Website: https://cervault.marsci-diagnostics.com/
- Downloads: https://cervault.marsci-diagnostics.com/download/
- Documentation: https://cervault.marsci-diagnostics.com/docs/
- Docker image: `ghcr.io/marsci-diagnostics/cervault:5.3.0-wave-d-preview.1`

## Docker installation

The Docker distribution is the headless CERVAULT governance runtime for Linux `amd64` and `arm64`. Native tray UI, login startup, desktop integration, and host-level controls remain in the platform installers.

```bash
docker pull ghcr.io/marsci-diagnostics/cervault:5.3.0-wave-d-preview.1

docker run -d --name cervault --restart unless-stopped \
  -p 127.0.0.1:8766:8766 \
  -e CERVAULT_CONTROL_PLANE_BEARER_TOKEN="replace-with-a-random-token-of-at-least-32-characters" \
  -v cervault-data:/var/lib/cervault \
  ghcr.io/marsci-diagnostics/cervault:5.3.0-wave-d-preview.1
```

CERVAULT requires the bearer token for non-loopback container traffic and serves HTTPS. On first start, the container generates a local self-signed TLS certificate in the persistent `cervault-data` volume; runtime state is stored in the same volume. Check local health with `https://127.0.0.1:8766/api/health` after trusting the local certificate; use a pinned version tag rather than a moving alias for controlled deployments.

## Platform policy

CERVAULT targets Windows x64/ARM64, Linux x64/ARM64, and macOS Intel/Apple Silicon. A target is listed as downloadable only after native build, runtime health, governed mutation, session lifecycle, no-orphan, package-boundary, and checksum acceptance has passed for that target.

## Repository boundary

This public repository intentionally does not contain CERVAULT confidential runtime source, private governance implementation, credentials, signing material, or internal evidence. It is a distribution surface, not the private development monorepo.


## Current public preview

**CERVAULT v5.3.0 Wave D Public Preview** is available for Windows x64/ARM64, Linux x64/ARM64, and macOS Intel/Apple Silicon.

- Release: https://github.com/MARSCI-DIAGNOSTICS/cervault/releases/tag/v5.3.0-wave-d-preview.1
- Integrity: `SHA256SUMS.txt` is attached to the release.
- Posture: acceptance-verified public preview; binaries are unsigned unless an asset explicitly states otherwise.

## Security

See [Security & Privacy](docs/SECURITY_AND_PRIVACY.md). Do not submit credentials or private customer/project data in public issues.

Copyright © 2026 CERVAULT. All rights reserved.
