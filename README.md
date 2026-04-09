# Human Design MCP Server

A remote MCP server for [Human Design](https://www.gethumandesign.com) — calculate bodygraph charts, explore your type, profile, strategy, authority, channels, centers, and gates, and compare charts for relationship dynamics.

## Features

- **Calculate charts** from any birth date, time, and place
- **Retrieve your own chart** instantly (no need to re-enter birth data)
- **Save people** — store birth data for family and friends
- **Compare charts** — relationship dynamics, electromagnetic channels, compatibility
- **Interactive bodygraph** — visual chart rendered in supporting clients
- **Adaptive depth** — explanations adjust to your Human Design experience level

## Setup

This is a remote MCP server — no local installation required. Connect your MCP client to the hosted endpoint using one of the methods below. Authentication is handled via OAuth 2.0 (you'll be prompted to sign in on first use).

### Claude Desktop

Add this to your `claude_desktop_config.json`:

```json
{
  "mcpServers": {
    "human-design": {
      "type": "streamable-http",
      "url": "https://api.gethumandesign.com/mcp"
    }
  }
}
```

### Claude Code (CLI)

```bash
claude mcp add human-design --transport streamable-http https://api.gethumandesign.com/mcp
```

### VS Code

Add this to your `.vscode/mcp.json` or user MCP configuration:

```json
{
  "servers": {
    "human-design": {
      "type": "streamable-http",
      "url": "https://api.gethumandesign.com/mcp"
    }
  }
}
```

### Cursor

Add this to your Cursor MCP settings:

```json
{
  "mcpServers": {
    "human-design": {
      "type": "streamable-http",
      "url": "https://api.gethumandesign.com/mcp"
    }
  }
}
```

### Windsurf

Add this to your Windsurf MCP settings:

```json
{
  "mcpServers": {
    "human-design": {
      "type": "streamable-http",
      "url": "https://api.gethumandesign.com/mcp"
    }
  }
}
```

## Tools

| Tool | Description |
|------|-------------|
| `calculate_chart` | Calculate a Human Design chart from a birth date, time, and place |
| `get_my_design` | Get the authenticated user's own chart |
| `get_person_design` | Get a saved person's chart by name |
| `compare_charts` | Compare two charts for relationship dynamics and compatibility |
| `list_people` | List all saved people in the user's account |
| `save_person` | Save a person's birth data for later retrieval |
| `remove_person` | Remove a saved person |

## Prompts

| Prompt | Description |
|--------|-------------|
| `analyze_my_design` | Comprehensive multi-step analysis of your Human Design chart |
| `compare_charts_guide` | Guided comparison of two charts for relationship dynamics |

## Links

- Website: [gethumandesign.com](https://www.gethumandesign.com)
- Support: hello@gethumandesign.com
