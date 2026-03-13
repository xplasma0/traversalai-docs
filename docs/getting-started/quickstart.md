# Quickstart (10-Minute Path)

This is the fastest safe path to first success.

## Step 1: Install

Install TraversalAI from the primary source repository or as a global CLI.

Primary source repository:

```bash
git clone https://github.com/xplasma0/traversalai-v2.git
cd traversalai-v2
corepack pnpm install
corepack pnpm build
```

## Step 2: Verify The CLI

```bash
traversalai --version
traversalai status
```

If you are running from a repo checkout instead of a global install, use:

```bash
node traversalai.mjs --version
node traversalai.mjs status
```

## Step 3: Complete Onboarding

```bash
traversalai onboard
```

## Step 4: Start The Gateway

```bash
traversalai gateway --force
```

## Step 5: Open The Chat Interface

```bash
traversalai chat --no-open
```

Open the printed URL in your browser.

## Step 6: Validate The Main Chat Features

Confirm that you can:

- send a prompt and receive a response
- switch agents
- switch models
- see tool activity
- see available skills from the gateway
- start a new chat and return to saved chats later

## Step 7: Save This Validation Checklist

- Onboarding completed
- Gateway running
- Chat interface reachable
- First response completed
- Agent and model switching working
- Saved chats visible

If any item fails, jump to [Troubleshooting](/traversalai-docs/docs/operations/troubleshooting).
