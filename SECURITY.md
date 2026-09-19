# Security Policy

## Reporting a vulnerability

**Do not open a public issue, discussion, or pull request for a security
problem.**

Use GitHub's private vulnerability reporting on this repository:

1. Open the **Security** tab.
2. Choose **Report a vulnerability**.
3. Describe the issue, the affected component, and the impact you believe it
   has.

If private reporting is unavailable, contact the maintainers through
[Navin Research](https://navinresearch.com) rather than posting publicly.

Please include, where you can:

- affected component and version or commit
- steps to reproduce, or a proof of concept
- what an attacker gains
- whether the issue requires a specific configuration or runtime
- any suggested mitigation

## What to expect

- We will acknowledge receipt as soon as we are able.
- We will confirm whether the report is accepted as a vulnerability and share an
  assessment of severity.
- We will keep you updated while a fix is prepared.
- We will credit you in the release notes if you want to be credited, and will
  respect your wish to stay anonymous.

Please give us reasonable time to ship a fix before any public disclosure.

## Why this matters here

OpenBot is a system that executes tools, terminal commands, browsers, file
operations, and — depending on configuration — work on remote machines and
infrastructure. A vulnerability in this project is not only a bug in a library;
it can mean arbitrary execution, secret exposure, or unauthorized action against
systems the user owns.

Report anything that could lead to:

- escaping a declared permission, policy, or approval boundary
- unauthorized tool, filesystem, network, or credential access
- leaking secrets into logs, artifacts, traces, or model context
- compromising isolation between workers, runs, tenants, or organizations
- tampering with run traces, audit records, or evaluation results
- supply-chain problems in packages, adapters, Cards, or Decks

## Scope

**In scope:** code and configuration shipped in this repository, plus the
protocols and policies they implement.

**Out of scope:** the behavior of third-party models, providers, harnesses,
runtimes, or MCP servers themselves. If a problem is caused by an upstream
dependency, report it upstream — but tell us too if OpenBot's own defaults or
integration amplify or hide it.

## Current status

This project is in early development and has no stable release yet.

**Do not deploy development builds into sensitive production environments.**
Assume that permission boundaries, isolation, and secret handling are still
being built and are not yet a security guarantee.

## Security model

For how permissions, approvals, memory access, secrets, runtime isolation, and
action recording are intended to work, see
[`docs/SECURITY.md`](./docs/SECURITY.md).
