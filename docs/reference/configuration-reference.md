# Configuration Reference

TraversalAI configuration is organized around runtime control, auth, integrations, and behavior policies.

## Core Sections

## Gateway

Primary runtime controls:

- mode
- bind address
- port
- remote/connectivity behavior

## Control UI

Dashboard behavior and host-header/auth posture:

- enable/disable UI
- auth requirements
- host header and trust policies

## Auth and Access

- token/password settings
- trusted-proxy-related identity policies
- device identity and secure-context constraints

## Channels

Channel-specific blocks define per-channel credentials, routing rules, and operational behavior.

## Providers and Models

Defines upstream model/provider behavior and credentials.

## Update Channel and Release Policy

Specifies stable/beta/dev update behavior and rollout intent.

## Environment Variable Mapping

Use environment overrides for deployment-specific values:

- secrets
- network topology
- environment-bound runtime options

## Configuration Safety Guidelines

- Keep one source of truth per environment
- Store secrets outside version control
- Apply least-privilege for all credentials
- Validate config changes with status/health probes
