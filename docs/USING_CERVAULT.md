# Using CERVAULT

CERVAULT is designed to stay in the background. The tray Quick Menu is the primary control surface; Control Center is for deeper setup, evidence, and diagnostics.

## Daily workflow

1. Confirm `Runtime: Healthy` in the tray.
2. Keep Governance in `Enforce` for normal governed work.
3. Confirm the AI client you intend to use is attached and idle.
4. Start the task through the CERVAULT-governed path rather than executing an untracked side effect directly.
5. Let CERVAULT lock the objective, target, acceptance criteria, and execution plan.
6. Review any required authorization before a side effect is allowed.
7. Inspect the final process gate, evidence, and reviewer outcome before treating the work as complete.

## What a governed task does

A governed task creates a persisted run before execution. CERVAULT routes the task to the declared repository scope, evaluates policy, issues only the bounded capability required for the approved operation, records a consumed receipt, and runs review plus deterministic acceptance.

If acceptance fails, remediation continues inside the same run instead of silently starting a new untracked attempt.

## Tray and Control Center

The Quick Menu surfaces Runtime, Governance, AI coverage, Members, Account, Activity, Settings, Refresh, and secondary stop/exit controls. Runtime health and AI coverage are deliberately separate: a healthy runtime does not claim that an AI client is attached.

Control Center is optional. Use it when you need first-run readiness, detailed client state, evidence, account projections, or diagnostics.

## Governance modes

`Enforce` is the safe default and the documented mode for governed work. CERVAULT also exposes `Guard` and `Observe` as operational controls, but they should only be selected when a documented workflow explicitly calls for them. Do not lower governance simply to get around a failed gate.

## Operations CERVAULT can govern

The current runtime supports bounded UTF-8 text writes, moves and copies, deterministic ZIP creation, allowlisted process execution, exact-path feature-branch commits, and non-force feature-branch pushes when policy and scope permit them.

CERVAULT denies main/master mutation, force push, free-form shell command text, unknown or overlapping repository scope, raw secrets, direct connector execution, and runless role execution.

## Evidence

Each governed run records the state needed to explain what was requested, what was authorized, what operation occurred, what evidence was produced, how review was performed, and whether acceptance passed.

CERVAULT evidence is a control record, not a claim that every AI output is factually correct. Analytical correctness still depends on the task inputs, evaluation criteria, and evidence used by the work itself.
