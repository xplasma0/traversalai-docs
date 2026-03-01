# Troubleshooting

Use this playbook for fast, high-confidence diagnosis.

## Incident Triage Flow

1. Confirm current symptom and affected surface
2. Check service health and reachability
3. Verify auth and pairing state
4. Validate channel/provider credentials
5. Inspect logs and recent config changes

## Common Scenarios

## Dashboard 404 / Unreachable

Checks:

- Is gateway process running?
- Is bind/port correct for the access path?
- Is reverse proxy/Tailscale route valid?
- Is dashboard URL token/auth valid?

## SSH Tunnel Connection Refused

Checks:

- Tunnel target matches active gateway bind (`127.0.0.1` vs tailnet IP)
- Remote gateway is listening on expected port
- Gateway mode did not change unexpectedly

## Auth Required / Unauthorized

Checks:

- Token/password in client matches gateway config
- Trusted-proxy mode has expected identity context
- Device identity requirements are satisfied

## Channel Delivery Failures

Checks:

- Channel credentials still valid
- Channel connection status healthy
- Routing and allowlist policies match expected target

## Provider/Model Failures

Checks:

- Provider credentials present and unexpired
- Endpoint reachability
- Model availability and allowed parameters

## Fast Command Set

Use this sequence:

1. `traversalai status`
2. `traversalai gateway status --deep`
3. `traversalai channels status --probe`
4. `traversalai logs` (or platform-specific log collection)

## Escalation Notes

Include in escalation report:

- exact error text
- command outputs used for verification
- recent config/deploy changes
- timestamp and environment scope
