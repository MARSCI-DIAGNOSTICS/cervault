# Get Started

CERVAULT v5.3 is validated on 64-bit Windows. The release panel behind the official CERVAULT Download action is the authority for supported operating systems and the current signed release.

## Requirements

- Windows 11 x64 for the currently validated release.
- Python 3.11 or newer available as `python` for the v5.3 runtime environment.
- .NET Desktop Runtime 8 is recommended for the full desktop shell; the tray fallback remains available when the desktop runtime is unavailable.
- Docker is not required.
- A model provider is not required to start CERVAULT, inspect status, or review local evidence. Model-backed tasks require a provider configured through the host environment.

## Install

1. Use the official CERVAULT website Download action and select the signed Windows release.
2. Keep the installer and its release verification material together when the release is distributed as a package bundle.
3. Start the installer. CERVAULT verifies the release before activation.
4. The v5.3 installer verifies the archive SHA-256 and package manifest, installs pinned dependencies from its offline wheelhouse, runs `pip check`, and executes the functional self-test.
5. When verification passes, CERVAULT starts the local runtime and exposes the tray Quick Menu.
6. Confirm the tray reports `Runtime: Healthy`.

Never bypass a failed hash, manifest, dependency, or self-test check. A failed verification means the candidate must not be activated.

## First run

1. Open the CERVAULT tray Quick Menu.
2. Confirm Runtime is healthy and Governance is set to `Enforce`.
3. Open **First-run readiness** from Control Center when deeper setup is needed.
4. Confirm launch-on-login preference and the available AI-client state.
5. Attach an eligible AI client.
6. If a model provider is configured, run the read-only sample task.
7. Review the task state, process gate, verdict, and evidence before starting real governed work.

First-run can be skipped and resumed. `NEEDS_PROVIDER_CONFIGURATION` means the local runtime is working but a model-backed task cannot run until a provider is configured.

## Reinstall and recovery

The release lifecycle supports verified reinstall, repair, update, rollback, and retained-data uninstall. CERVAULT backs up the previous installation before replacement and rolls back when candidate verification or self-test fails.

Downgrades require explicit authorization. CERVAULT must never leave duplicate tray or runtime instances after an update.

## Next

Continue with [Using CERVAULT](USING_CERVAULT.md).
