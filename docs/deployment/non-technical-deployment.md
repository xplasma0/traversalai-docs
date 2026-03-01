# Non-Technical Deployment Guide

This is a full end-to-end deployment guide written for operators with minimal technical background.

## Goal

Get TraversalAI running and reachable from your browser with a safe setup.

## 1. Choose Where to Run It

You have two practical choices:

## Option A: Cloud VM (recommended)

- Better uptime
- Easier remote access
- Cleaner separation from personal devices

## Option B: Personal always-on machine

- Fast to start
- Good for home labs and personal usage

## 2. Install Runtime

Follow [Installation](/traversalai-docs/docs/getting-started/installation).

After install, verify:

```bash
traversalai --version
traversalai status
```

## 3. Configure Access Safely

Start with local-only binding and secure access path.

Recommended pattern:

- Bind gateway to loopback
- Use trusted tunnel/reverse proxy for remote access
- Keep auth enabled

## 4. Start Service

Start the gateway process using your environment’s service strategy.

Then validate:

```bash
traversalai gateway status --deep
```

You want to see:

- Runtime: running
- RPC probe: ok
- Listening endpoint matches your intended bind

## 5. Open Dashboard

Use:

```bash
traversalai dashboard --no-open
```

Open the printed URL in browser.

## 6. Pair Device (if prompted)

```bash
traversalai devices list
traversalai devices approve <requestId>
```

## 7. Validate Health

Run:

```bash
traversalai status
traversalai channels status --probe
```

## 8. Keep It Stable

Weekly checks:

- Confirm service still running
- Confirm auth still enforced
- Review logs for repeated errors
- Back up config and session state

## 9. Safe Upgrade Process

Use [Upgrade Guide](/traversalai-docs/docs/operations/upgrade-guide).

Never upgrade without backup.

## 10. Common Failure Recovery

- Dashboard unreachable: check bind/port and tunnel route
- Unauthorized: refresh token/password and pairing
- Channel not delivering: check credentials and channel health

See full: [Troubleshooting](/traversalai-docs/docs/operations/troubleshooting)
