<div align="center">

# Navin OpenBot

**Start with the work, not the stack.**

Navin OpenBot brings together the right crew, models, harnesses, tools, and machines around the job, with every part yours to configure, replace, and shape however you want.

[Website](https://navinresearch.com) · Documentation · Marketplace · Community

</div>

---

> **Project Status**
>
> OpenBot is in early development.
>
> The architecture, interfaces, and core concepts described here represent both working components and the direction of the project. Features that are not ready yet are marked accordingly.

## What is OpenBot?

OpenBot is a place to hand off real work.

Give it a job and it can bring together the people-shaped roles, models, tools, harnesses, and machines needed to carry that work through.

You can keep things simple with one worker and one task, or build a complete crew with different roles, tools, permissions, memory, and ways of working.

Nothing important has to be fixed.

Change the model. Replace the harness. Move execution from your laptop to a server. Swap a tool. Change how memory works. Add another worker. Remove one. Build your own runtime.

OpenBot is meant to adapt around the work instead of forcing the work into one stack.

## Why OpenBot?

The agent ecosystem is growing quickly, but most tools still make an early decision for you.

One model.

One harness.

One computer.

One workflow.

One way of organizing agents.

OpenBot takes a different approach.

The job comes first.

```text
                         JOB
                          │
                    OpenBot Router
                          │
          ┌───────────────┼───────────────┐
          │               │               │
        Crew            Harness         Runtime
          │               │               │
      Researcher       Codex           Local
      Builder          Claude Code     Cloud
      Reviewer         OpenCode        VPS
      Operator         Pi              Sandbox
                       OpenHands       Remote
          │               │               │
          └───────────────┼───────────────┘
                          │
                    Tools + Memory
                          │
                       Result
```

OpenBot is designed so every layer can evolve independently.

## Built around the work

### Any model

Use the models that make sense for the task.

OpenBot is being designed around provider-neutral model interfaces, including hosted APIs, local models, and compatible custom endpoints.

The long-term goal is not simply to support many models.

It is to let different work use different intelligence.

### Any harness

A model does not have to be the worker.

OpenBot treats agent harnesses as replaceable execution layers.

The same system may eventually route work through:

* Native OpenBot workers
* Claude Code
* Codex
* OpenCode
* Pi
* OpenHands
* compatible third-party harnesses
* custom harness adapters

A coding job may use a coding harness.

Research may use a different one.

A private task may stay entirely local.

### Any machine

Execution should happen where it makes sense.

OpenBot is being designed for:

* local computers
* cloud machines
* user-owned VPS instances
* isolated sandboxes
* remote hosts
* GPU machines
* private infrastructure
* edge devices

The default experience should remain simple.

```text
Run on: Auto
```

Advanced users can control every part.

## Crew

OpenBot calls a working group a **Crew**.

A Crew can contain one worker or many.

Each member can have its own:

* role
* instructions
* model
* harness
* tools
* memory
* permissions
* runtime
* budget
* approval rules

A simple task may only need one worker.

A product task might form something like:

```text
                 Lead
                  │
       ┌──────────┼──────────┐
       │          │          │
   Research     Builder    Reviewer
                              │
                              QA
```

The Crew can change with the job.

## Cards

Cards are reusable pieces of an OpenBot setup.

They provide a common way to package capability without forcing everything into one giant configuration file.

### Agent Card

Defines a role that can perform work.

Examples:

```text
Researcher
Builder
Reviewer
QA
Operator
```

### Model Card

Defines intelligence available to a worker.

### Skill Card

Defines a reusable way of completing a task.

### Tool Card

Connects a worker to a tool or external system.

### Memory Card

Provides reusable knowledge or context.

### Runtime Card

Defines where work can execute.

### Policy Card

Defines what a worker may and may not do.

### Trigger Card

Defines when work begins.

### Trap Card

Defines a condition that interrupts or redirects work.

For example:

```text
IF production deployment

THEN
  pause
  snapshot
  review
  request approval
```

### Brain Card

Provides an alternative decision or execution system.

Brain Cards are also where experimental Navin Research work can connect to OpenBot.

## Decks

A **Deck** is a portable working setup.

Instead of configuring every worker, tool, model, permission, and workflow manually, a Deck can package them together.

For example:

```text
Product Builder Deck

Crew
  Planner
  Builder
  Reviewer
  QA

Skills
  Repository Analysis
  Implementation
  Browser Verification
  Release Review

Tools
  Terminal
  Browser
  GitHub

Memory
  Project Context
  Engineering Guidelines

Policies
  No production deployment without approval

Runtime
  Local or isolated sandbox
```

A user should be able to start with:

```text
Equip Deck
```

and customize anything later.

## Ways to work

### Solo

One person and one worker.

Use it when the job is straightforward.

### Cowork

You remain inside the loop and work alongside OpenBot.

Intervene whenever you want.

### Dual

One worker does the job.

Another checks it independently.

```text
Builder
   +
Reviewer
```

### Team

Multiple specialized workers collaborate on the same outcome.

### Arena

Run different configurations against the same job.

Compare:

* models
* harnesses
* workers
* Skills
* Decks
* routing strategies

Use the same task, constraints, and budget.

Measure the result instead of guessing.

## Learn from the work

OpenBot should not solve the same problem from zero forever.

The learning loop is:

```text
Reason
   ↓
Execute
   ↓
Verify
   ↓
Learn
   ↓
Reuse
```

When a workflow succeeds, OpenBot can preserve what mattered.

Repeated work can gradually move from expensive general reasoning toward reusable execution.

```text
Reasoning
   ↓
Skill
   ↓
Workflow
   ↓
Tool calls / scripts
   ↓
Procedural execution
```

The general model remains available when something new or uncertain happens.

The goal is simple:

**Use reasoning where reasoning is useful. Reuse what already works.**

## Skills

Skills capture repeatable ways of working.

A Skill may contain:

* instructions
* tools
* decision rules
* validation
* expected outputs
* permissions
* examples
* tests

OpenBot's longer-term direction goes beyond storing Skills as prompt files.

Skills should be testable, versioned, measurable, and eventually compilable into more efficient forms where possible.

## Memory

Different kinds of memory should not all live in one bucket.

OpenBot is being designed around scoped memory.

```text
User
  │
Organization
  │
Workspace
  │
Project
  │
Crew
  │
Worker
  │
Task
  │
Temporary Context
```

Memory can carry ownership, provenance, permissions, confidence, and lifetime.

A worker should only see what it needs.

## Routing

OpenBot should be able to decide more than which model to call.

Routing may consider:

```text
task
complexity
cost
latency
privacy
available tools
runtime
historical success
context requirements
permissions
```

The router can then select:

```text
Worker
Model
Harness
Runtime
Tools
```

Manual control remains available.

## Tools and integrations

OpenBot is being designed to work with both direct integrations and open tool protocols.

Planned integration paths include:

* MCP
* APIs
* command-line tools
* browsers
* desktop applications
* local programs
* custom tools

If there is no direct integration, computer use can provide another path.

## Human control

Autonomy should have boundaries.

OpenBot is being designed around explicit permissions and approval points.

Examples:

```text
Sending email           Ask first
Production deployment   Ask first
Deleting data            Ask first
GitHub read              Allow
GitHub write             Scoped
External network         Restricted
Maximum task cost        $5
```

Different workers can have different permissions.

A researcher does not need production access.

A deployment worker does not need every company secret.

## Runs, replay, and evaluation

A useful system should be able to explain what happened.

OpenBot aims to make runs inspectable.

A run may record:

* worker
* model
* harness
* runtime
* tools
* handoffs
* cost
* latency
* outputs
* retries
* approvals
* failures

Runs should eventually support:

```text
Inspect
Replay
Fork
Compare
Retry
```

This also provides the foundation for evaluating Skills, Decks, workers, and routing policies.

## Marketplace

The OpenBot Marketplace is planned as a place for reusable working systems, not only prompts.

Possible packages include:

* Cards
* Decks
* Skills
* Tools
* MCP integrations
* workflows
* memory packs
* policies
* evaluators
* datasets
* runtime adapters
* harness adapters

Creators should eventually be able to:

```text
Publish
Fork
Remix
Version
Benchmark
Share
```

Marketplace packages should carry useful technical information such as compatibility, permissions, dependencies, version history, and evaluation results.

## Portability

OpenBot should earn retention through usefulness, not by making work difficult to move elsewhere.

The project is being designed around portable components.

Long-term work includes specifications for reusable Cards and Decks that can be exported, versioned, shared, and implemented by other tools.

Nothing here is presented as a finalized standard yet.

## Experimental intelligence

OpenBot also provides a place for experimental work from Navin Research.

**Synomorph** explores whether successful repeated behavior can move from general reasoning into specialized procedural systems.

Candidate approaches include:

* deterministic workflows
* small policy models
* reservoir systems
* spiking systems
* synthetic neural structures
* biologically inspired networks

These systems are not assumed to be better than general models.

They have to earn their place through evaluation.

General reasoning remains responsible for novelty.

Specialized systems are explored for repeated, constrained, low-latency, embodied, or edge workloads.

## Architecture

The planned architecture separates the pieces that are usually bundled together.

```text
                       Navin OpenBot
                             │
                         Job Graph
                             │
                       Smart Router
                             │
             ┌───────────────┼───────────────┐
             │               │               │
           Crew            Harness         Runtime
          Router            Router          Router
             │               │               │
       Roles / Cards    Agent systems    Local / Cloud
             │               │           VPS / Sandbox
             └───────────────┼───────────────┘
                             │
                        Execution Bus
                             │
              ┌──────────────┼──────────────┐
              │              │              │
             MCP          Browser         Terminal
             API          Computer        Files
              │              │              │
              └──────────────┼──────────────┘
                             │
                    Memory + Artifacts
                             │
                     Policy + Approval
                             │
                      Traces + Evals
                             │
                       Skill Learning
```

The architecture is intentionally modular.

No single model, harness, runtime, or provider should become a permanent dependency of the whole system.

## Project status

OpenBot is currently being built.

The roadmap is roughly divided into the following stages.

### Foundation

* [ ] Core worker runtime
* [ ] Task/session model
* [ ] Provider abstraction
* [ ] Tool execution
* [ ] Local filesystem
* [ ] Terminal
* [ ] Basic web interface
* [ ] Configuration system

### Crew

* [ ] Multiple workers
* [ ] Parallel execution
* [ ] Worker-to-worker messages
* [ ] Task handoff
* [ ] Shared workspace
* [ ] Scoped memory
* [ ] Human interruption

### Runtime

* [ ] Local runtime
* [ ] Docker runtime
* [ ] Remote runtime
* [ ] Cloud sandbox adapters
* [ ] Runtime routing

### Harnesses

* [ ] Native OpenBot
* [ ] Codex adapter
* [ ] Claude Code adapter
* [ ] OpenCode adapter
* [ ] Pi adapter
* [ ] OpenHands adapter

### Cards and Decks

* [ ] Card specification
* [ ] Deck format
* [ ] Import / export
* [ ] Deck editor
* [ ] Versioning

### Learning

* [ ] Skill capture
* [ ] Teach a Task
* [ ] Run replay
* [ ] Skill evaluation
* [ ] Skill optimization
* [ ] Habit compilation

### Marketplace

* [ ] Public registry
* [ ] Package discovery
* [ ] Install / update
* [ ] Fork / remix
* [ ] Verified evaluations
* [ ] Creator publishing

### Research

* [ ] Synomorph runtime experiments
* [ ] Procedural policy experiments
* [ ] Adaptive compute experiments
* [ ] Alternative Brain Cards

The roadmap will change as the project develops.

## Quick Start

OpenBot is not ready for a stable public installation yet.

Installation instructions will be added when the first usable release is available.

For development builds, see the development documentation in this repository.

## Development

Development instructions will be added as the initial repository structure stabilizes.

The intended workflow will include:

```bash
git clone <repository>
cd Navin-OpenBot

# install dependencies
# configure providers
# start development environment
```

Exact commands will be documented when the bootstrap process is stable.

## Documentation

Documentation will be organized around:

| Area            | Purpose                                          |
| --------------- | ------------------------------------------------ |
| Getting Started | From installation to the first completed job     |
| Crew            | Workers, roles, handoffs, and collaboration      |
| Models          | Providers, local models, and routing             |
| Harnesses       | External worker runtimes and adapters            |
| Runtimes        | Local, cloud, VPS, sandbox, and remote execution |
| Cards           | Reusable OpenBot components                      |
| Decks           | Portable working configurations                  |
| Skills          | Teaching and reusing workflows                   |
| Memory          | Scope, storage, permissions, and retrieval       |
| Security        | Policies, secrets, approvals, and isolation      |
| Marketplace     | Publishing and installing components             |
| Development     | Architecture, APIs, and contribution guides      |
| Research        | Experimental intelligence and Synomorph          |

## Contributing

OpenBot is being developed in the open.

Contributions will be welcome across:

* core runtime
* provider adapters
* harness adapters
* runtime adapters
* tools and MCP integrations
* Skills
* Cards and Decks
* evaluation
* security
* documentation
* UI
* research

Before submitting a large implementation, open an issue or discussion so the architecture can be agreed on first.

A dedicated `CONTRIBUTING.md` will contain development setup, code style, testing, and pull request requirements.

## Security

OpenBot executes tools, commands, browsers, and potentially remote systems.

Security issues should not be reported through public issues.

A dedicated `SECURITY.md` will document the responsible disclosure process before the first public release.

Until then, do not deploy development builds into sensitive production environments.

## Community

OpenBot is a project from **Navin Research**.

Website: https://navinresearch.com

Community links and project discussions will be added as they become available.

## Research

Some parts of OpenBot are also research questions.

We are interested in:

* adaptive model and harness routing
* long-horizon work
* agent reliability
* procedural memory
* skill compilation
* evaluation and replay
* memory architecture
* runtime isolation
* multi-worker coordination
* learning from successful trajectories
* biological and synthetic control systems

Research prototypes are kept separate from production claims.

## License

License information will be added before the first public release.

If you plan to use, redistribute, or build on OpenBot, check the repository license before doing so.

## Acknowledgements

OpenBot is influenced by the broader open agent ecosystem and the people building it.

Projects worth studying include:

* Hermes Agent
* Pi
* OpenClaw
* DeerFlow
* OpenHands
* Agent Zero
* Letta
* Browser Use
* MCP and the open tooling ecosystem

OpenBot intends to build alongside that ecosystem rather than hide it behind a closed stack.

---

<div align="center">

**Start with the work, not the stack.**

Built by Navin Research.

</div>
