# Installation

This guide is written for both technical and non-technical operators.

## 1. Prerequisites

- A Linux or macOS machine
- Node.js 22 or newer
- Internet access for model providers and package install
- A terminal account with permissions to run long-lived processes

Check your versions:

```bash
node --version
corepack --version
```

## 2. Install the CLI (recommended)

```bash
npm install -g traversalai@latest
traversalai --version
```

Run onboarding:

```bash
traversalai onboard --install-daemon
```

Open the dashboard URL without launching a browser automatically:

```bash
traversalai dashboard --no-open
```

## 3. Run from source (developer workflow)

```bash
git clone https://github.com/xplasma0/traversalai.git
cd traversalai
corepack pnpm install
```

Use these quality-gate commands:

```bash
corepack pnpm build
corepack pnpm test:fast
corepack pnpm lint
corepack pnpm tsgo
corepack pnpm format:check
corepack pnpm audit --prod
```

## 4. Local run commands

```bash
corepack pnpm openclaw status
corepack pnpm openclaw dashboard --no-open
```

To chain into a follow-up command from dashboard context:

```bash
corepack pnpm openclaw dashboard devices list
```

## 5. Common operator checks

```bash
traversalai status
traversalai gateway status --deep
traversalai channels status --probe
```

## 6. Production notes

- Pin CLI versions in production environments.
- Keep backup and recovery steps documented per environment.
- Prefer explicit environment variables over hardcoded secrets.
