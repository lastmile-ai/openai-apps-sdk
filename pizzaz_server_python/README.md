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
uv run mcp-agent deploy --no-auth
```

## Testing in ChatGPT
To add these apps to ChatGPT, enable [developer mode](https://platform.openai.com/docs/guides/developer-mode), and add your apps in Settings > Connectors.

> [!IMPORTANT]
> Make sure to have `/sse` at the end of your url to connect to your server

## Try a hosted version now
MCP Server URL: `https://18t536mliucyeuhkkcnjdavxtyg66pgl.deployments.mcp-agent.com/sse`
