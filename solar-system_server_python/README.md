# Hosting OpenAI's ChatGPT App - Solar-System MCP server (Python)

This repository contains [OpenAI's Solar System MCP server](https://github.com/openai/openai-apps-sdk-examples/tree/main/solar-system_server_python) (python) with a one line change to get it hosted onto [mcp-agent cloud](https://www.mcp-agent.com/)

This enables the OpenAI Solar-system demo application to be hosted and used by anyone.

## Prerequisites

- Python 3.10+

## Installation

We recommend using [uv](https://docs.astral.sh/uv/) for a fast Python package manager.
```bash
uv init
uv sync
```

Alternatively, you can use `pip` by adding a new `requirements.txt` in `solar-system_server_python`.
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
MCP Server URL: `https://1iolks0szy0x0grtu8509imb90uizpq6.deployments.mcp-agent.com/sse`
