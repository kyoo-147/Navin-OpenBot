# Contributing to Navin OpenBot

Thanks for taking the time to look at this project.

## Project stage

OpenBot is in **early development**. The architecture and interfaces are still
being defined, and large parts of the system described in the README and in
[`docs/`](./docs) are **planned rather than implemented**.

Because of that, please read [Project status](./README.md#project-status) and
[`docs/PRODUCT.md`](./docs/PRODUCT.md) before proposing anything substantial.
Do not infer what is shipped from the vision documents — check the code.

## Before you write code

For anything larger than a small fix, **open an issue or a discussion first** so
the design can be agreed on before implementation. This avoids work that has to
be thrown away because it locks the project into a direction it is explicitly
trying not to take.

## Design principles

These come from the product thesis and are the most common reason a change is
asked to be reworked:

1. **Work first, stack second.** The job defines the configuration, not the
   other way around.
2. **Every important layer is replaceable.** No permanent dependency on one
   model provider, one harness, one runtime, one browser engine, or one memory
   backend.
3. **Prefer adapters and explicit interfaces** over provider-specific logic in
   core.
4. **Simple by default, deeply configurable when needed.** Advanced
   configuration is optional, never mandatory.
5. **Permissions, secrets, approvals, and runtime isolation are first-class.**
   Not a deployment-time afterthought.
6. **Everything autonomous is attributable** to a run, worker, tool, and policy
   decision.
7. **Evaluation beats intuition.** Claims about quality, cost, or reliability
   should be measurable.
8. **Research stays separate from product claims.**

Please avoid: unnecessary framework rewrites, all-in-one worker classes, hidden
global state, implicit permissions, untraceable routing, and marketing copy in
technical documentation.

## Status language

When you touch documentation or UI, use these labels consistently:

| Label | Meaning |
| --- | --- |
| **Available** | Implemented and usable |
| **Preview** | Implemented but unstable or incomplete |
| **Planned** | Accepted direction, not shipped |
| **Experimental** | Research or prototype path |
| **Concept** | Design proposal, not yet committed |

Never silently turn a planned feature into a shipped claim.

## Contribution areas

Contributions are welcome across:

- core runtime
- provider adapters
- harness adapters
- runtime adapters
- tools and MCP integrations
- Skills
- Cards and Decks
- evaluation and replay
- security and policy
- documentation
- UI
- research

## Development setup

A bootstrap process does not exist yet, so there is no install/build/test
workflow to document. This section will be filled in when the initial repository
structure stabilizes.

## Submitting changes

1. Fork the repository and create a branch from `main`.
2. Keep the change focused — one concern per pull request.
3. Describe **what** changed and **why**, and note anything you deliberately did
   not do.
4. Update documentation that your change makes inaccurate.
5. Link the issue or discussion that agreed the direction, when one exists.

If a change alters a core concept, say so explicitly in the pull request
description rather than letting it land as an implementation detail.

## Definition of done

For a substantial capability, a pull request is expected to include:

1. a clear interface
2. the implementation
3. permissions and security behavior
4. trace or event visibility
5. tests
6. failure behavior
7. documentation
8. status updated in the roadmap

Not every small change needs all eight. Core concepts do.

## Communication

Be direct about technical disagreements — the project would rather hear that an
approach is wrong now than discover it later. See
[`CODE_OF_CONDUCT.md`](./CODE_OF_CONDUCT.md) for the standard expected in
project spaces.

## License

By contributing, you agree that your contributions are licensed under the
[Apache License 2.0](./LICENSE), and that you have the right to submit them.
