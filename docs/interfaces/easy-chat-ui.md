# Easy Web Chat UI

This is the simplest gateway-backed chat interface for TraversalAI.

It is designed for users who want a clean workflow with visible controls and persistent chat sessions.

## What It Includes

- Connects through the TraversalAI gateway
- Switch between agents
- Switch between connected models
- View available tools and skills from the gateway
- Start a new chat without destroying previous sessions
- Reopen saved chats and continue them later
- Delete saved chats from the sidebar

## Run It From The CLI

```bash
traversalai chat --no-open
```

Open the local URL printed by the command.

If you are testing from a source checkout:

```bash
node traversalai.mjs chat --no-open
```

## Run It Against A Specific Gateway

```bash
traversalai chat --no-open --url ws://127.0.0.1:28789 --token <token>
```

## Typical Workflow

1. Complete onboarding.
2. Start the gateway.
3. Open chat.
4. Send a request.
5. Change the active agent or model if needed.
6. Watch tool activity in the UI when tools run.
7. Return to saved chats later to continue the same session.

## Troubleshooting

- If the page opens but no response appears, confirm the gateway is running and retry through a fresh chat session.
- If agents or models are missing, verify gateway configuration and run `traversalai status`.
- If the CLI command is not available, test with `node traversalai.mjs chat --no-open` from the repository root.
- If you changed local frontend code, rebuild before testing the packaged chat flow.

## Notes

- Agent changes use gateway session semantics.
- Model changes are applied per session through the gateway.
- Tool and skill lists are loaded from the same gateway APIs as the main chat path.
- Saved chat deletion removes the stored non-main session from the gateway-backed session list.
