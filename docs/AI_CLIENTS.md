# AI Clients

CERVAULT is designed to govern external AI clients rather than force users into a single model or assistant.

## Validated client families

The v5.3 compatibility matrix has completed bounded read-only governed tasks with:

- Claude Code 2.1.220
- Gemini CLI 0.53.0
- Codex / ChatGPT CLI 0.146.0
- OpenClaw 2026.7.2-beta.7

All four validated client families registered with the AI Client Gateway, completed the bounded task, passed the process gate, and produced zero repository mutation in the compatibility run.

## What attachment means

A client is not considered governed simply because its application is running. CERVAULT uses client identity, admission state, heartbeat, session state, and task attachment to determine coverage.

Typical coverage states include:

- `UNATTACHED` — no eligible governed client is attached.
- `ATTACHED_IDLE` — a client is attached and ready, with no active governed task.
- `GOVERNED` — governed work is active through the CERVAULT path.

In `Enforce` mode, client freshness is checked before governed execution.

## Client-specific configuration

Compatibility is proven for the tested client versions and bounded invocation conditions. It does not mean every user-specific extension, shell alias, local configuration, or provider setup is automatically valid.

If a client cannot attach, CERVAULT must report the client-side repair boundary separately from runtime health. It should not silently weaken governance or mutate the client's saved configuration just to make a test pass.

## Model providers

CERVAULT does not require a model-provider credential to start the local runtime, inspect status, or review evidence. Model-backed task execution requires a provider supplied through a host-owned provider surface.

Provider credentials are not entered into CERVAULT first-run UI and should not be embedded in task payloads, evidence, or repository content.

## Adding another client

A new client integration should prove stable identity, bounded registration, heartbeat, admission, session attachment, workspace-mutation evidence where required, task completion, and clean detachment. Support should be claimed only after that compatibility path has evidence.
