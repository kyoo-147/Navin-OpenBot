# AGENTS.md

Instructions for coding and research agents working on Navin OpenBot.

## Read Order

Before substantial work, read:

1. `PROJECT_CONTEXT.md`
2. `docs/PRODUCT.md`
3. the domain-specific document relevant to the task

Do not infer shipped status from product vision. Check implementation before claiming a feature exists.

## Working Rules

- Preserve the product thesis: **work first, stack second**.
- Do not hard-code the architecture around one model provider.
- Do not hard-code the architecture around one agent harness.
- Do not hard-code execution to one machine or sandbox provider.
- Prefer adapters and explicit interfaces over provider-specific logic in core.
- Keep the beginner path simple; advanced configuration should be optional.
- Treat permissions, secrets, approvals, and runtime isolation as first-class concerns.
- Every autonomous action should be attributable to a run, worker, tool, and policy.
- Prefer measurable behavior over marketing claims.
- Keep production capabilities and research experiments separated.
- Do not introduce new abstractions unless they reduce complexity or enable clear portability.

## Terminology

Preferred product language:
- **Crew** — working group
- **Worker** — an executable role/member of a Crew
- **Card** — reusable component
- **Deck** — portable working configuration
- **Run** — one execution instance
- **Harness** — agent execution framework/runtime
- **Runtime** — machine/environment where execution occurs

Use `agent` when required by technical interoperability, APIs, protocols, or external ecosystem terminology.

## Feature Status

When adding docs or UI:
- Available
- Preview
- Planned
- Experimental
- Concept

Never silently convert a planned feature into a shipped claim.

## Design Constraints

OpenBot should remain:

- provider-neutral
- harness-neutral
- runtime-neutral
- portable
- observable
- permission-aware
- human-steerable

## Avoid

- unnecessary framework rewrites
- giant all-in-one worker classes
- hidden global state
- implicit permissions
- magic routing without traceability
- marketing copy in technical docs
- artificial lock-in
- unbenchmarkable self-modification
- experimental biological claims presented as product fact

## Definition of Done

For a substantial capability, prefer to have:

1. clear interface
2. implementation
3. permissions/security behavior
4. trace/event visibility
5. tests
6. failure behavior
7. documentation
8. status updated in `docs/ROADMAP.md`

If the capability changes a core concept, also update `PROJECT_CONTEXT.md`.
