# Why CERVAULT

AI agents can plan, call tools, edit files, run commands, and coordinate work quickly. The harder problem is proving that the work stayed inside the intended objective, scope, authority, and acceptance criteria.

CERVAULT is built for that control problem.

## What it adds

- A persisted run exists before governed execution begins.
- Objective, target, acceptance criteria, and plan are locked as task state.
- Side effects pass a deterministic pre-action authorization gate.
- Repository scope is resolved through explicit manifests instead of inferred from convenience.
- Approved operations receive bounded, exact-argument capabilities rather than unrestricted tool authority.
- Executed operations produce receipts that are consumed into the run evidence.
- Self-review and independent review are separated from execution.
- Deterministic acceptance decides whether the run can close.
- Failed acceptance can remediate inside the same run, preserving continuity and evidence.
- AI-client heartbeat and coverage distinguish an actually governed client from an application that merely happens to be open.

## CERVAULT vs a typical agent harness

| Concern | Typical orchestration-first harness | CERVAULT |
|---|---|---|
| Primary job | Coordinate models, agents, and tools | Govern execution and prove control state |
| Run state | May be transient or workflow-specific | Persisted before governed execution |
| Objective and scope | Often prompt/workflow driven | Explicitly locked and checked |
| Tool access | Tool or connector permission | Policy decision plus bounded capability |
| Side effects | Executed by the workflow | Pre-authorized and receipted |
| Review | Optional agent step | Separate review plus deterministic acceptance |
| Failed result | Retry or start another workflow | Same-run remediation with continuity |
| Client presence | App/process may be treated as available | Registration, heartbeat, admission, and coverage |
| Repository mutation | Depends on agent/tool policy | Explicitly bounded; high-risk mutations denied by default |

This is an architectural comparison, not a claim that every other harness lacks governance features. Some platforms implement overlapping controls. CERVAULT's distinction is that governance state, authorization, evidence, review, and acceptance are first-class runtime responsibilities rather than optional prompting conventions.

## When CERVAULT is useful

Use CERVAULT when an AI can change files, invoke tools, touch repositories, operate across multiple agents, or produce work that must be reviewed and evidenced before acceptance.

If you only need a conversational assistant with no meaningful side effects or audit requirement, a governance runtime may add more process than you need.
