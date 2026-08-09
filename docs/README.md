# CERVAULT Docs

CERVAULT is a governed execution layer for AI work. It sits between an AI client and the actions that can change a project, so work is planned, authorized, evidenced, reviewed, and accepted before it is treated as complete.

CERVAULT does not replace Claude, Gemini, ChatGPT/Codex, OpenClaw, or another AI client. It provides the control layer around them.

## Start here

1. [Get Started](GET_STARTED.md) — install CERVAULT and complete first-run readiness.
2. [Using CERVAULT](USING_CERVAULT.md) — tray, Control Center, governed tasks, and evidence.
3. [Why CERVAULT](WHY_CERVAULT.md) — what it adds beyond a normal agent harness.
4. [AI Clients](AI_CLIENTS.md) — validated client families and attachment boundaries.
5. [Security & Privacy](SECURITY_AND_PRIVACY.md) — local runtime, credentials, repository, and IP boundaries.
6. [Troubleshooting & FAQ](TROUBLESHOOTING.md) — common states and recovery steps.

## The operating model

```text
AI client
  ↓
CERVAULT session
  ↓
Objective + scope + acceptance lock
  ↓
Pre-action authorization
  ↓
Bounded capability / operation
  ↓
Evidence + receipt
  ↓
Independent review
  ↓
Deterministic acceptance gate
  ↓
Complete or remediate in the same run
```

## Safe defaults

- Keep Governance in `Enforce` for normal governed work.
- Use the tray Quick Menu as the primary control surface.
- Treat `Healthy` runtime state and AI-client coverage as separate signals.
- Install only signed releases published through the official CERVAULT download channel.
- Do not use unsigned validation artifacts as a normal installation.

CERVAULT v5.3 is currently validated on Windows. Platform support published on the download page is the authority for each public release.
