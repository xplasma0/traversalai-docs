# Installation

## Prerequisites

- Linux or macOS workstation/server
- Node.js 22+
- `corepack` enabled for `pnpm`
- Network access to your model and provider endpoints

## Install From Source

Use this path if you are running the current primary repository directly:

```bash
git clone https://github.com/xplasma0/traversalai-v2.git
cd traversalai-v2
corepack pnpm install
corepack pnpm build
node traversalai.mjs --help
```

This validates that the source checkout builds and that the local CLI entrypoint works.

## Install As a CLI Program

If you want the `traversalai` command in your shell:

```bash
npm install -g .
traversalai --help
```

## First-Time Setup

Run onboarding before opening chat or the dashboard:

```bash
traversalai onboard
```

## Verify

```bash
traversalai --version
traversalai status
traversalai chat --no-open
```

## Notes

- `node traversalai.mjs ...` is the safest repo-local path.
- `traversalai ...` is the installed CLI path.
- Keep runtime and UI builds aligned when testing local source changes.
- Pin versions in production.
