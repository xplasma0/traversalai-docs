# Production Hardening

This guide defines a practical baseline for secure production operation of TraversalAI.

## Required Controls

## Network Exposure

- Do not expose raw gateway ports publicly without auth and filtering
- Prefer private network overlays or trusted reverse proxies
- Restrict ingress with explicit allowlists

## Authentication and Identity

- Enforce strong auth for control surfaces
- Rotate tokens and shared credentials regularly
- Avoid shared long-lived credentials across environments

## Secrets Management

- Keep secrets out of repository history
- Use dedicated secret storage per environment
- Scope provider tokens to minimum required permissions

## Host Hardening

- Apply host OS updates and security patches
- Run services with minimum required privileges
- Lock down unnecessary outbound/inbound paths

## Observability and Auditability

- Enable structured logging and retention policies
- Alert on repeated auth failures and suspicious activity
- Preserve operational audit trails for incident response

## Recommended Enhancements

- Segment runtime from edge ingress layers
- Use immutable deployment patterns where possible
- Implement staged rollout + rollback controls

## Change Management

Before production rollout:

1. Validate in staging
2. Confirm security policy alignment
3. Run smoke checks (`status`, `gateway status --deep`)
4. Document rollback path
