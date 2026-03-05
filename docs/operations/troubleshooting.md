# Troubleshooting

This playbook focuses on high-frequency operational issues and exact fixes.

## A. `dashboard devices list` says "too many arguments"

If you are on an older build, you may see this parser error.

Use:

```bash
corepack pnpm build
corepack pnpm openclaw dashboard devices list
```

Expected behavior:

- dashboard URL is printed first
- `devices list` runs as a follow-up command

## B. `pnpm: command not found` during build

Symptom often appears in source workflows where `corepack pnpm build` triggers scripts that internally call `pnpm`.

Use:

```bash
corepack pnpm build
```

If it still fails, confirm:

```bash
corepack --version
node --version
```

## C. Dashboard not reachable over SSH tunnel

Typical cause: tunnel target and gateway bind mismatch.

Recommended tunnel:

```bash
ssh -L 28789:127.0.0.1:28789 user@gateway-host
```

Notes:

- New CLI hints may intentionally show `gateway-host` instead of a private server IP.
- Replace `gateway-host` with the public DNS name or reachable IP you actually use for SSH.

Then open:

- `http://localhost:28789/`

Verify listener on the remote host:

```bash
ss -ltnp | grep 28789
```

## D. Tailscale IP returns "connection refused"

Check these in order:

1. Gateway process is running.
2. Gateway bind mode allows your network path.
3. Firewall/security-group allows the port.
4. Tunnel target matches the bind address.

## E. Pairing or authorization issues

```bash
traversalai devices list
traversalai devices approve <requestId>
traversalai status
```

If needed, regenerate auth token and retry from a fresh dashboard URL.

## F. Incident bundle for support

Collect and share:

- output of `traversalai status`
- output of `traversalai gateway status --deep`
- exact error text
- timestamp with timezone
- last config or deployment change before failure
