# Glossary

## OpenBot
The overall Navin system for executing and coordinating work across models, harnesses, tools, workers, and runtimes.

## Job
The outcome the user wants completed.

## Task
A unit of work inside a Job.

## Run
One execution instance with traceable inputs, decisions, actions, and outputs.

## Worker
An executable role/member that performs work.

## Crew
One or more workers organized around a Job.

## Agent
Use when referring to external ecosystem terminology, protocols, libraries, or APIs. Product-facing OpenBot language may prefer Worker/Crew.

## Model
A language, multimodal, vision, or other model used for inference.

## Provider
A service or local backend that serves models.

## Harness
A framework/runtime that wraps a model with tools, context, loops, policies, and execution behavior.

Examples: native OpenBot, Codex, Claude Code, OpenCode, Pi, OpenHands.

## Runtime
The machine/environment where work executes.

Examples: local machine, cloud VM, Docker, sandbox, VPS, remote host, GPU node.

## Tool
A capability available to a Worker, such as terminal, browser, API, GitHub, Figma, Gmail, or MCP server.

## Skill
A reusable method for completing a class of tasks.

## Memory
Persisted context/knowledge available according to scope and permissions.

## Card
A reusable OpenBot component.

## Deck
A portable configuration that packages the components required for a class of work.

## Policy
A rule that allows, denies, limits, or requires approval for behavior.

## Trigger
An event or schedule that starts work.

## Trap
A conditional control that pauses, redirects, stops, or escalates work.

## Brain
A decision/execution runtime. May be a general LLM or an experimental specialized system.

## Artifact
A file, report, message, code change, screenshot, log, dataset, or other output produced by work.

## Router
The component that selects or validates workers, models, harnesses, runtimes, and tools.

## Arena
A controlled comparison mode where multiple configurations receive the same task, constraints, and budget.

## Synomorph
Navin Research direction exploring specialized procedural and biologically inspired intelligence for constrained/repeated behavior.
