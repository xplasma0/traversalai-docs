# Dashboard

The TraversalAI dashboard is the primary operational interface for live control.

## Purpose

Use the dashboard to:

- Verify gateway health and connectivity
- Operate sessions and chats in real time
- Review runtime logs and background activity
- Manage pairing, tokens, and access workflow
- Inspect channels, agents, and execution approvals

## Main Views

## Overview

Shows current gateway state, access settings, and quick health signals.

## Chat

Primary operator surface for interacting with active sessions.

## Sessions

Session list with identity/context continuity for long-running workflows.

## Usage

Token and provider usage metrics, including trend-oriented summaries.

## Channels

Current channel states and connectivity behavior.

## Logs / Debug

Structured runtime diagnostics used for triage and incident response.

## Secure Access Patterns

Recommended production access patterns:

1. Use loopback binding and reverse proxy/Tailscale for remote usage
2. Keep auth enabled for control UI endpoints
3. Rotate dashboard tokens regularly
4. Restrict dashboard ingress to trusted identities

## Device Pairing Model

Device pairing is used when new clients request dashboard access under protected gateway policy.

Typical flow:

1. Client requests pairing
2. Operator lists pending devices
3. Operator approves request ID
4. Client receives access token path

## Operational Checklist

Before daily use:

- Confirm gateway health is `ok`
- Confirm auth mode is expected
- Confirm active sessions are valid
- Confirm no stale critical errors in logs
