<p align="center">
  <img src="https://cervault.marsci-diagnostics.com/assets/cervault-logo-ui-400.png" alt="CERVAULT logo" width="180" />
</p>

<h1 align="center">CERVAULT</h1>

<p align="center"><strong>Local-first AI agent governance harness for controlled, auditable AI execution.</strong></p>

<p align="center">
  Pre-action authorization · AI agent guardrails · bounded tool execution · evidence trails · recovery controls
</p>

<p align="center">
  <a href="https://cervault.marsci-diagnostics.com/">Website</a> ·
  <a href="https://cervault.marsci-diagnostics.com/docs/">Docs</a> ·
  <a href="https://github.com/MARSCI-DIAGNOSTICS/cervault/releases/tag/v5.3.0-wave-d-preview.1">Latest preview</a> ·
  <a href="https://github.com/MARSCI-DIAGNOSTICS/cervault/issues">Feedback & issues</a>
</p>

> **Public preview:** CERVAULT v5.3.0 Wave D is available for Windows, macOS, and Linux on x64 and ARM64. Preview binaries are currently unsigned unless an individual asset explicitly states otherwise.

## Why CERVAULT?

AI coding agents and autonomous tools can move faster than a human can review every action. Prompt instructions alone are not an execution boundary. CERVAULT adds a governed layer around AI work so actions can be authorized, constrained, recorded, and recovered before a tool changes the environment.

CERVAULT is designed for teams and builders who want **AI agents with guardrails**, not unrestricted automation.

### What it does

- **Pre-action authorization** — evaluate an intended action before execution instead of auditing only after the fact.
- **Bounded execution** — constrain approved file, archive, process, feature-branch Git, and other supported operations.
- **Governed task execution** — run work through explicit task, policy, remediation, and evidence states.
- **Audit evidence** — retain structured run and decision evidence so a result can be reviewed after execution.
- **Same-run remediation** — recover from bounded failures without silently widening authority.
- **Multi-repository routing** — govern work that spans more than one repository while preserving scope boundaries.
- **Local runtime and desktop surface** — use CERVAULT on the machine where AI tools and repositories actually run.

## Download CERVAULT

You do **not** need to go through the website. The six current preview builds can be downloaded directly from GitHub Releases.

| Platform | Architecture | Direct download |
|---|---|---|
| Windows 10/11 | x64 | [CERVAULT-win-x64-v5.3.0.zip](https://github.com/MARSCI-DIAGNOSTICS/cervault/releases/download/v5.3.0-wave-d-preview.1/CERVAULT-win-x64-v5.3.0.zip) |
| Windows 10/11 | ARM64 | [CERVAULT-win-arm64-v5.3.0.zip](https://github.com/MARSCI-DIAGNOSTICS/cervault/releases/download/v5.3.0-wave-d-preview.1/CERVAULT-win-arm64-v5.3.0.zip) |
| macOS | Apple Silicon / ARM64 | [CERVAULT-osx-arm64-v5.3.0.zip](https://github.com/MARSCI-DIAGNOSTICS/cervault/releases/download/v5.3.0-wave-d-preview.1/CERVAULT-osx-arm64-v5.3.0.zip) |
| macOS | Intel / x64 | [CERVAULT-osx-x64-v5.3.0.zip](https://github.com/MARSCI-DIAGNOSTICS/cervault/releases/download/v5.3.0-wave-d-preview.1/CERVAULT-osx-x64-v5.3.0.zip) |
| Linux | x64 | [CERVAULT-linux-x64-v5.3.0.zip](https://github.com/MARSCI-DIAGNOSTICS/cervault/releases/download/v5.3.0-wave-d-preview.1/CERVAULT-linux-x64-v5.3.0.zip) |
| Linux | ARM64 | [CERVAULT-linux-arm64-v5.3.0.zip](https://github.com/MARSCI-DIAGNOSTICS/cervault/releases/download/v5.3.0-wave-d-preview.1/CERVAULT-linux-arm64-v5.3.0.zip) |

Verify the archive before use with [SHA256SUMS.txt](https://github.com/MARSCI-DIAGNOSTICS/cervault/releases/download/v5.3.0-wave-d-preview.1/SHA256SUMS.txt).

### Quick start

1. Download the archive for your OS and CPU architecture above.
2. Verify its SHA-256 checksum against `SHA256SUMS.txt`.
3. Extract the archive.
4. Follow the platform instructions bundled with the preview package and the [CERVAULT documentation](https://cervault.marsci-diagnostics.com/docs/).
5. Keep the preview limitations below in mind before giving an AI tool access to important repositories or production systems.

## How CERVAULT fits around an AI agent

```text
User / Project
      │
      ▼
AI agent or coding assistant
      │ proposes action
      ▼
┌──────────────────────────────┐
│           CERVAULT           │
│  identity + scope + policy   │
│  pre-action authorization    │
│  bounded execution           │
│  evidence + recovery         │
└──────────────────────────────┘
      │ authorized action
      ▼
Files · Git · processes · tools
```

CERVAULT is not another foundation model. It is an **AI agent harness / governance runtime** around model-driven work.

## When it is useful

CERVAULT is a good fit when you need to:

- let an AI coding agent work while keeping mutation scope explicit;
- separate executor authority from review and policy decisions;
- preserve evidence of what an agent attempted and what was actually authorized;
- operate across multiple repositories without treating every repository as one unrestricted workspace;
- make AI-assisted work recoverable instead of relying on a successful prompt every time;
- add execution governance without replacing the model or agent you already use.

It is **not** intended to turn every AI assistant into an unrestricted shell or to bypass repository, credential, production, or security controls.

## CERVAULT vs adjacent tool categories

CERVAULT overlaps with several categories, but the control point is different.

| Category | Typical strength | Typical gap CERVAULT addresses |
|---|---|---|
| Prompt/system instructions | Fast behavioral guidance | Instructions are not a hard execution boundary |
| AI observability / tracing | Excellent post-run visibility | Often observes after an action has already happened |
| Workflow automation | Connects tools and automates steps | Automation does not inherently provide per-action governance |
| Sandbox/container isolation | Strong environment isolation | Isolation alone does not express task authority, policy, or evidence semantics |
| **CERVAULT** | **Pre-action governance + bounded execution + evidence** | Adds control around supported agent actions while remaining model-agnostic |

This is not a claim that CERVAULT replaces all observability, sandboxing, IAM, CI/CD, or security products. Those controls remain complementary.

## Preview limitations

CERVAULT is still a public preview. Current boundaries are intentional:

- preview binaries are unsigned unless an asset explicitly states otherwise;
- supported operations are bounded rather than unrestricted shell/source mutation;
- CERVAULT does not grant automatic main-branch, force-push, or destructive production authority;
- connector coverage depends on the connected client and the operation being governed;
- production credentials and external service permissions remain the responsibility of the operator;
- do not treat the preview as a substitute for backups, repository protection, IAM, endpoint security, or independent review.

## Docker headless runtime

A headless Linux container build exists for `amd64` and `arm64`. The native tray UI, login startup, desktop integration, and host-level controls remain in the platform packages.

**Current distribution note:** the GHCR package has been built and multi-architecture acceptance passed, but anonymous public pull is not yet enabled. Until package visibility is changed, use the native GitHub Release downloads above. Do not rely on the Docker command in unattended public installation scripts yet.

## Security & privacy

CERVAULT's public repository deliberately excludes confidential governance source, private control-plane implementation, credentials, signing material, and internal evidence.

- [Security & Privacy](docs/SECURITY_AND_PRIVACY.md)
- Never post API keys, passwords, signing keys, payment-card data, customer secrets, or production credentials in GitHub Issues.

## Feedback, bugs, and feature requests

The preferred public feedback channel is **GitHub Issues** so reports can be tracked instead of disappearing into email threads:

- [Report a bug](https://github.com/MARSCI-DIAGNOSTICS/cervault/issues/new?template=bug_report.yml)
- [Request a feature](https://github.com/MARSCI-DIAGNOSTICS/cervault/issues/new?template=feature_request.yml)
- [Browse existing issues](https://github.com/MARSCI-DIAGNOSTICS/cervault/issues)

For account, billing, or privacy matters that should not be public, use the [support page](https://cervault.marsci-diagnostics.com/support/).

## Search terms / project scope

CERVAULT is relevant to: **AI agent governance, AI agent harness, agent guardrails, AI safety runtime, LLM guardrails, execution governance, agent security, policy engine, governed AI execution, autonomous agent controls, coding-agent safety, AI audit trail, local-first AI governance, and agentic AI security**.

## Release integrity

The current release surface is [CERVAULT v5.3.0 Wave D Public Preview](https://github.com/MARSCI-DIAGNOSTICS/cervault/releases/tag/v5.3.0-wave-d-preview.1). Each published target includes SHA-256 artifact metadata and was admitted through target-specific native acceptance before publication.

Copyright © 2026 CERVAULT. All rights reserved.
