# CLI

The TraversalAI CLI is the authoritative automation surface for scripting, diagnostics, and operations.

## CLI Principles

- Deterministic behavior for automation
- Machine-readable output where applicable
- Fast operational feedback for incident handling

## Core Command Areas

## Runtime and Connectivity

- `gateway`: service lifecycle and connectivity
- `dashboard`: local control-UI tokenized launch
- `status`: health snapshot and troubleshooting hints

## Sessions and Messaging

- `agent` / `agents`: agent lifecycle and interaction
- `message`: send and inspect message flows
- `sessions`: session state operations

## Configuration and Security

- `config` / `configure`: configuration state and guided setup
- `security`: security checks and guardrail surfaces
- `doctor`: environment diagnostics and remediation hints

## Integrations and Extensibility

- `channels`: channel state and controls
- `plugins`: plugin lifecycle and management
- `hooks`: automation hook introspection and control

## Operational Usage Patterns

## Local Diagnostics

1. `traversalai status`
2. `traversalai gateway status --deep`
3. `traversalai channels status --probe`

## Access Recovery

1. `traversalai dashboard --no-open`
2. `traversalai devices list`
3. `traversalai devices approve <requestId>`

## Safe Automation

- Prefer explicit command flags over implicit defaults in CI
- Use non-interactive flows for repeatable environments
- Capture command output into structured logs
