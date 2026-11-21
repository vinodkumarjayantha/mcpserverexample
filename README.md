# MCP Server Deep Dive Deployment

A minimal Python MCP server built with the MCP Python SDK. It exposes an `add`
tool that returns the sum of two integers.

## Requirements

- Python 3.11 or newer
- [uv](https://docs.astral.sh/uv/)

## Use with an MCP client

Add the following server entry to your MCP client's configuration. The client
uses `uvx` to fetch the project from GitHub and run it without a separate
checkout or local installation:

```json
{
  "Deployment": {
    "command": "uvx",
    "args": [
      "--from",
      "git+https://github.com/vinodkumarjayantha/mcpserverexample.git",
      "mcp-server-deepdive-deployment"
    ]
  }
}
```

The exact configuration file location depends on the MCP client. Restart or
reload the client after updating its configuration. Once connected, the server
provides the `add` tool described below.

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
