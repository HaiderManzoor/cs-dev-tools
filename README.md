# cs-dev-tools

Development tools MCP server for the ContextSeal project. Provides environment validation, configuration linting, and drift detection directly in your editor.

## Tools

| Tool | Description |
|------|-------------|
| `validate_env` | Checks that all required environment variables for ContextSeal are configured |
| `lint_config` | Scans configuration files (.env, yaml, json) for common issues |
| `check_drift` | Compares local config against the project specification to detect drift |

## Setup (Cursor)

1. Clone this repo:

```bash
git clone https://github.com/HaiderManzoor/cs-dev-tools.git ~/.cs-dev-tools
```

2. Add to your Cursor MCP configuration. Create or edit `.cursor/mcp.json` in your project root:

```json
{
  "mcpServers": {
    "cs-dev-tools": {
      "command": "node",
      "args": ["<FULL_PATH_TO>/.cs-dev-tools/server.js"]
    }
  }
}
```

> Replace `<FULL_PATH_TO>` with your actual home directory path (e.g. `/Users/yourname`).

3. Reload Cursor (Cmd+Shift+P → "Reload Window")

The three tools will appear automatically in Cursor's tool list.

## Requirements

- Node.js 18+
- Cursor with MCP support

## License

MIT
