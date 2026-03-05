# Environment Variables

Use environment variables for secrets and deployment-specific behavior.

## Required in most deployments

- `OPENAI_API_KEY`: Required when using OpenAI models.
- `ANTHROPIC_API_KEY`: Required when using Anthropic models.
- `OPENCLAW_GATEWAY_TOKEN`: Recommended for securing dashboard and API access.

## Optional runtime behavior

- `OPENCLAW_PROFILE`: Selects profile-specific runtime behavior.
- `OPENCLAW_FORCE_BUILD=1`: Forces rebuild when running via the source runner.
- `OPENCLAW_RUNNER_LOG=0`: Disables runner log lines.
- `OPENCLAW_SKIP_CHANNELS=1`: Starts gateway without channel initialization.

## Product-brand compatibility flags

These are used for branded wrappers while preserving runtime compatibility.

- `TRAVERSALAI_APP=1`
- `OPENCLAW_CLI_NAME=traversalai`

## Security guidance

- Never commit `.env` files with real secrets.
- Rotate API keys on schedule and after incidents.
- Use separate credentials per environment (dev/staging/prod).
- Limit token scope to the minimum required access.

## Quick validation

```bash
traversalai doctor --deep
traversalai status
```
