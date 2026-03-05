# Command Reference

This reference maps the TraversalAI CLI surface by operational domain.

## Global Pattern

- `traversalai <command> [subcommand] [options]`
- `traversalai <command> --help` for command-specific flags

## Runtime

### `gateway`

Manage and inspect gateway runtime.

Use for:

- start/restart flows
- deep status checks
- connection troubleshooting

### `dashboard`

Open control UI with current auth/token context.

Use for:

- obtaining the exact tokenized access URL
- local secure launch operations
- forwarding into a follow-up command after URL output

Examples:

```bash
traversalai dashboard --no-open
traversalai dashboard devices list
```

### `status`

Summarize health across runtime, channels, and dependencies.

Use for:

- rapid triage
- pre-change safety checks

## Access and Pairing

### `devices`

Pairing and device approval operations.

Use for:

- listing pending requests
- approving request IDs
- enforcing controlled dashboard access

### `qr`

QR-oriented onboarding and connection convenience flows.

## Configuration

### `config`

Raw configuration management operations.

### `configure`

Guided setup and targeted section editing.

## Maintenance

### `doctor`

Performs environment and runtime diagnostics with action hints.

### `update`

Checks and applies runtime updates according to release policy.

## Integrations

### `channels`

Channel status and operational controls.

### `plugins`

Plugin inspection, enablement, and operational checks.

### `hooks`

Hook metadata and lifecycle-aware diagnostics.

## Advanced

### `sandbox`

Execution safety and sandbox policy interactions.

### `nodes`

Node-level orchestration and distributed-control workflows.

### `logs`

Operational log inspection and quick diagnostics.
