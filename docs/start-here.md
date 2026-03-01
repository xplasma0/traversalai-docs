# Start Here (For Non-Technical Users)

This guide assumes you are not a software engineer.

By the end, you will have:

- TraversalAI installed
- Dashboard opening in your browser
- A working first command
- A safe baseline configuration

## Before You Begin

You need only 3 things:

1. A machine that is always on (cloud VM or home computer)
2. Your terminal access (copy/paste commands)
3. 20-30 minutes

## Step 1: Install TraversalAI

Use the installation method documented in the installation guide.

If someone gave you a ready command, paste that exactly.

## Step 2: Start the Gateway

Run the command to start gateway service.

If you are unsure, check:

- [Quickstart](/traversalai-docs/docs/getting-started/quickstart)
- [Self-Hosting](/traversalai-docs/docs/deployment/self-hosting)

## Step 3: Open Dashboard

Run:

```bash
traversalai dashboard --no-open
```

Open the URL it prints.

## Step 4: If Pairing Is Required

Run:

```bash
traversalai devices list
traversalai devices approve <requestId>
```

Then refresh the dashboard.

## Step 5: Send First Message

In the dashboard chat box, ask a simple command:

- "show me system status"
- "list my active sessions"

## Step 6: Lock Down Security

At minimum:

- Keep dashboard private
- Use token/password auth
- Do not expose raw control ports to the public internet

Read: [Security and Auth](/traversalai-docs/docs/configuration/security-and-auth)

## If Something Breaks

Use the troubleshooting flow:

- [Troubleshooting](/traversalai-docs/docs/operations/troubleshooting)

You can safely follow it line by line.
