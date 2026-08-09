# Troubleshooting & FAQ

## Runtime is healthy but no AI client is available

This is not a runtime failure. Check client coverage separately. Open the tray or Control Center and confirm whether the client is `UNATTACHED`, `ATTACHED_IDLE`, or actively governed.

## First-run says `NEEDS_PROVIDER_CONFIGURATION`

CERVAULT is running, but a model-backed task cannot execute until a provider is configured through the host-owned provider surface. Do not paste provider credentials into first-run, task prompts, or repository files.

## A client is detected but cannot attach

Treat client repair separately from CERVAULT runtime health. Verify the client version, local configuration, shell/CLI invocation, heartbeat, admission state, and any required workspace-mutation evidence. Do not disable governance to force attachment.

## Installation stops on hash or manifest verification

Do not continue with that artifact. Download the signed release again from the official channel and verify you are using the matching release files.

## Installation stops during dependency or self-test checks

The candidate must not be activated. Use Repair only with the same trusted release source, or restore the previous verified version through the release lifecycle.

## Two tray or runtime instances appear

CERVAULT considers duplicate runtime or tray instances an invalid lifecycle result. Stop the duplicate instance and use the verified repair/recovery path rather than starting additional copies manually.

## Can I downgrade?

Downgrades require explicit authorization because they can change the trust and compatibility assumptions of the installed runtime. Use a recorded rollback to a verified previous installation when recovery is required.

## Can I use CERVAULT without a browser?

Yes. The tray is the primary surface and the browser UI is optional diagnostics.

## Can I use CERVAULT without Docker?

Yes. The current Windows runtime does not require Docker.

## Does CERVAULT make AI output correct?

No. CERVAULT governs process, scope, authorization, evidence, review, and acceptance. Factual or analytical correctness still depends on the task's data, evidence, evaluation design, and the behavior of the AI/model being used.

## Does CERVAULT replace my AI client?

No. It is a governance and execution-control layer around supported AI clients.

## Where should I start after a problem?

Check in this order: runtime health → governance mode → client coverage → current run state → process gate/evidence → client/provider-specific diagnostics. Keep the previous verified installation available until the new candidate has passed activation and self-test.
