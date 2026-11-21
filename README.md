# MCP Server Deep Dive Deployment

A minimal Python MCP server built with the MCP Python SDK. It exposes an `add`
tool that returns the sum of two integers.

## Requirements

- Python 3.11 or newer
- [uv](https://docs.astral.sh/uv/)

## Install

From the project directory, install the project and its dependencies:

```shell
uv sync
```

## Run

Start the server over standard input/output:

```shell
uv run mcp-server-deepdive-deployment
```

The server can also be started as a Python module:

```shell
uv run python -m mcp_server_deepdive_deployment
```

## Available tool

### `add`

Adds two integer inputs:

| Input | Type |
| --- | --- |
| `a` | integer |
| `b` | integer |

The tool returns `a + b`.
