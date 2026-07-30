# Amanuel's Daily Plugins

A personal Claude Code plugin marketplace for daily-workflow assistants.

## Plugins

| Plugin | How it helps | Connectors |
|--------|--------------|------------|
| **[daily-assistant](./daily-assistant)** | Summarize your inbox, draft replies to messages that need one, and turn today's calendar into a simple timetable. | Gmail, Google Calendar (native connectors) |

## Getting Started

```bash
# Add the marketplace
claude plugin marketplace add amanuelmeharzghi/claude-plugins

# Install a plugin
claude plugin install daily-assistant@amanuel-daily-plugins
```

Once installed, skills activate automatically when relevant — e.g. asking "catch me up on email" triggers `summarize-emails`.

## How Plugins Work

Every plugin follows the same structure:

```
plugin-name/
├── .claude-plugin/plugin.json   # Manifest
├── .mcp.json                    # Tool connections
├── README.md                    # What it does, how to use it
└── skills/                      # Domain knowledge Claude draws on automatically
```

- **Skills** encode step-by-step workflows Claude follows when relevant — no need to invoke them explicitly.
- **Connectors** wire Claude to external tools. `daily-assistant` relies on claude.ai's native Gmail and Google Calendar connectors rather than a bundled MCP server, so its `.mcp.json` is intentionally empty.

Every component is file-based — markdown and JSON, no code, no build steps.
