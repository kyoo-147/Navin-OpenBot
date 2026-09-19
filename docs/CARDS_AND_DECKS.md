# Cards and Decks

## Card

A Card is a reusable OpenBot component.

Cards should be:
- identifiable
- versionable
- portable
- inspectable
- permission-aware
- composable
- evaluable where meaningful

## Card Types

### Agent Card
Defines a worker role.

Typical fields:
- name
- purpose
- instructions
- default model/harness
- skills
- tools
- memory scope
- permissions
- budget
- approval rules

### Model Card
Defines a model/provider configuration and capabilities.

### Skill Card
Defines a reusable method for completing a class of task.

### Tool Card
Defines access to a tool, application, API, MCP server, CLI, or capability.

### Memory Card
Packages reusable knowledge/context with scope and permissions.

### Runtime Card
Defines an execution environment.

### Policy Card
Defines allowed, denied, or approval-gated behavior.

### Trigger Card
Starts work from time, event, webhook, message, file, repository change, or other supported trigger.

### Trap Card
Interrupts or redirects a run when a condition is met.

Examples:
- production deployment → pause and request approval
- cost exceeds budget → stop
- secret exposure suspected → isolate and escalate

### Brain Card
Defines an alternative decision/execution runtime.

General LLMs are one possible source of intelligence; experimental specialized runtimes may also exist.

## Fusion

Multiple Cards can be composed into a higher-level capability.

Example:

`Researcher + Builder + Reviewer → Product Builder configuration`

Fusion is a composition concept, not necessarily a separate technical primitive.

## Deck

A Deck is a portable working configuration for a class of jobs.

A Deck can contain:

- Crew
- Agent Cards
- Model Cards
- Skill Cards
- Tool Cards
- Memory Cards
- Runtime Cards
- Policy Cards
- Trigger Cards
- Trap Cards
- evaluators
- harness configuration
- routing rules

## Example

```text
Website Builder Deck
├─ Crew
│  ├─ Planner
│  ├─ Frontend
│  ├─ Backend
│  └─ Reviewer
├─ Skills
│  ├─ Repository Analysis
│  ├─ UI Implementation
│  └─ Browser Verification
├─ Tools
│  ├─ Browser
│  ├─ Terminal
│  └─ GitHub
├─ Runtime
│  └─ Auto
├─ Memory
│  └─ Project Context
└─ Policy
   └─ Production deployment requires approval
```

## UX Goal

Beginner:
`Equip Deck → give job`

Power user:
open the Deck and replace any component.

## Portable Format

Potential future file concepts:
- `.opencard`
- `.deck`

These are concepts, not finalized standards.

A future specification may include:
- kind
- name
- version
- requirements
- permissions
- compatibility
- dependencies
- evaluation metadata
- provenance
