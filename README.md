# project-context-mcp

MCP server that provides workspace context, persistent development notes, project scaffolding, and development directives across sessions.

## Install

### Windsurf (One-Click)
[Install in Windsurf](windsurf://windsurf-mcp-registry?serverName=io.github.mubtaxim/project-context)

### Manual (Windsurf / Cursor / VS Code)
Add to your `mcp_config.json`:

```json
{
  "mcpServers": {
    "project-context": {
      "command": "npx",
      "args": ["-y", "@mubtaxim/project-context-mcp"]
    }
  }
}
```

## Tools

| Tool | Description |
|------|-------------|
| `ctx_get_context` | Scan workspace files, read docs, return project architecture and active directives |
| `ctx_save_note` | Save a persistent development note with tags |
| `ctx_get_notes` | Retrieve notes from previous sessions |
| `ctx_init_project` | Scaffold a new project with AGENTS.md from a description |
| `ctx_set_directive` | Set a per-workspace development directive |
| `ctx_set_global_directive` | Set a global directive for all workspaces |

## Data Storage

Notes and directives are stored locally at `~/.mcp-context/`:

```
~/.mcp-context/
├── directives.json           # Active directives
└── workspaces/
    ├── {hash}.json            # Per-workspace notes
    └── ...
```

## License

MIT
