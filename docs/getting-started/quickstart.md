# Quickstart (10-Minute Path)

This is the fastest safe path to first success.

## Step 1: Install

Install TraversalAI runtime and CLI.

## Step 2: Verify

```bash
traversalai --version
traversalai status
```

## Step 3: Start Gateway

Start service and verify deep status:

```bash
traversalai gateway status --deep
```

## Step 4: Open Dashboard URL

```bash
traversalai dashboard --no-open
```

Open the printed URL in your browser.

## Step 5: Pair if Needed

```bash
traversalai devices list
traversalai devices approve <requestId>
```

## Step 6: First Command

In dashboard chat, run a simple request and confirm response.

## Step 7: Save This Validation Checklist

- Gateway running
- Dashboard reachable
- Auth working
- First command completed

If any item fails, jump to [Troubleshooting](/traversalai-docs/docs/operations/troubleshooting).
