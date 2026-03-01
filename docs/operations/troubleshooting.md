# Troubleshooting

This page is written as a decision tree for non-technical and technical users.

## A. Dashboard does not open

### Check A1: Is service running?

Run:

```bash
traversalai gateway status --deep
```

Expected:

- Runtime is running
- RPC probe is ok

### Check A2: Is URL correct?

Use:

```bash
traversalai dashboard --no-open
```

Copy the exact URL again.

### Check A3: Tunnel/path mismatch?

If using SSH tunnel, ensure gateway bind matches tunnel target.

Common error:

- Tunnel points to `localhost`, gateway listens on tailnet IP

## B. Unauthorized / auth required

### Check B1: Token/password in client

- Token exists and matches gateway config
- Password is current

### Check B2: Pairing pending

```bash
traversalai devices list
traversalai devices approve <requestId>
```

## C. Channel messages not arriving

### Check C1: Channel health probe

```bash
traversalai channels status --probe
```

### Check C2: Credentials expired

Refresh tokens/keys for affected channel.

## D. After upgrade, behavior changed

Use [Upgrade Guide](/traversalai-docs/docs/operations/upgrade-guide) and compare config + release notes.

## E. Fast Incident Bundle (copy this to support)

Include:

- output of `traversalai status`
- output of `traversalai gateway status --deep`
- exact error message text
- timestamp and timezone
- what changed just before failure
