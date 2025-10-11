# Hosting OpenAI's ChatGPT App - Pizzaz MCP server (Python)

This repository contains [OpenAI's Pizzaz MCP server](https://github.com/openai/openai-apps-sdk-examples/tree/main/pizzaz_server_python) (python) with a one line change to get it hosted onto [mcp-agent cloud](https://www.mcp-agent.com/)

This enables the OpenAI Pizzaz demo application to be hosted and used by anyone.

https://github.com/user-attachments/assets/cb50700c-5650-4f12-ac2e-2eabba5c8144

## Prerequisites

- Python 3.10+

## Installation

We recommend using [uv](https://docs.astral.sh/uv/) for a fast Python package manager.
```bash
uv init
uv sync
```

Alternatively, you can use `pip` by adding a new `requirements.txt` in `pizzaz_server_python`.
```bash
pip install mcp-agent
pip install fastapi
```

## Deploy the application

```bash
uv run mcp-agent login
uv run mcp-agent deploy
```

Save your `mcp-agent cloud auth token` and your `app_id` for the next step.

## Allow users to use your app with authentication

Add in your `mcp-agent cloud auth token` and your `app_id` to the curl command below to turn off authentication. 

Execute the command in your terminal:
```bash
curl -X PUT -H "Authorization: Bearer [mcp-agent cloud token]" https://mcp-agent.com/api/mcp_app/update_app -d '{"app_id": "fill-in-your-id", "unauthenticatedAccess": true}'
```

Example:
```bash
curl -X PUT -H "Authorization: Bearer lm_mcp_api_ey232345iJkwefwefweflbmMiOiJBMwefw0NNIn0..a2v1e8Qwef42dTqdlP.S4nCryFi737SV9WbieNasdffwef1x1asdfasdasdfmFV3jgFuLzasdefd3FxG1bmfhqcDNUgsOyF6xt-3kk-u0zdRk_dpB9wtFtkFZuWhgMKk2W0Jv8wSk2vmRLasdf9V0-eawehasdf09GwOK43dDsVQ_crCAasdfDc_PGwWKxasdfrRmBKN-7vZSts7878asdfmRyQ" https://mcp-agent.com/api/mcp_app/update_app -d '{"app_id": "app_9acdaf01-1234-dcba-abcd-1234567890", "unauthenticatedAccess": true}'
```

## Testing in ChatGPT
To add these apps to ChatGPT, enable [developer mode](https://platform.openai.com/docs/guides/developer-mode), and add your apps in Settings > Connectors.

