# Easy Web Chat UI

This is the simplest chat interface for TraversalAI.

It is designed for people who want a clean, easy workflow with clear controls.

## What It Includes

- Connect to your gateway with URL + token
- Switch between agents
- Switch between connected models
- Start a new chat and stop running responses
- View available tools and skills from the gateway

## Where It Lives In The Code

- `ui/technical.html`
- `ui/src/technical/technical-app.ts`
- `ui/src/technical/technical.css`
- `ui/vite.technical.config.ts`

## Run It Locally

From the TraversalAI repo:

```bash
pnpm ui:dev:technical
```

Open:

- `http://localhost:5174/technical.html`

## Notes

- This runs on a separate port (`5174`) so it does not conflict with the main control UI.
- Model changes are applied per session through gateway session patching.
- Tool and skill lists are loaded from the same gateway APIs as the main UI.
