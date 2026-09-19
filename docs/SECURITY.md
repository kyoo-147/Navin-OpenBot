# Security and Control Model

## Principle

**Autonomous where it helps. Human where it matters.**

## Security Is a Product Layer

Security must not be added only at deployment time.

Every worker/run should be constrained by explicit capability and policy boundaries.

## Permission Areas

- filesystem
- network
- browser
- terminal
- APIs
- MCP tools
- secrets
- repositories
- external messages
- production systems
- payments/spending
- token/cost budgets
- runtime access

## Approval Examples

Require explicit approval for:
- production deployment
- sending external communication
- purchasing/spending
- destructive deletion
- permission changes
- secret changes
- legal acceptance
- sensitive account actions

## Scoped Secrets

Secrets should be:
- scoped to the smallest practical worker/project/runtime
- masked from unnecessary logs
- inaccessible to workers that do not need them
- auditable when used

## Runtime Isolation

OpenBot should support different isolation levels:
- local trusted execution
- containers
- isolated sandbox/VM
- remote/private runtime

Isolation is a policy choice per task, worker, or organization.

## Network Policy

Support:
- unrestricted
- allowlist
- denylist
- no external network
- local/private-only

## Memory ACL

Memory should have explicit:
- owner
- scope
- readers/writers
- provenance
- lifetime

Sharing a Crew must not imply sharing all secrets or memory.

## Action Recording

Important actions should be traceable:
- command
- tool call
- browser action
- connector action
- permission decision
- approval
- handoff
- artifact change

## Policy / Trap Examples

```text
IF deployment_target == production
THEN snapshot + review + request approval
```

```text
IF estimated_cost > task_budget
THEN pause + notify
```

```text
IF secret_exposure_detected
THEN stop + isolate + escalate
```

## Self-Optimization Safety

OpenBot may propose candidate changes, but should not silently rewrite production behavior.

Preferred flow:

`observe → propose → evaluate → shadow test → compare → approve/promote`

## Reporting

Before public release, the repository should contain a dedicated responsible disclosure process.

Do not ask users to report sensitive vulnerabilities in public issues.
