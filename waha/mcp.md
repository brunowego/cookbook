# WAHA MCP

## Adding

```sh
# User Level
claude mcp add --transport http -s user waha http://localhost:3000/mcp \
  --header 'X-Api-Key: <MCP_APP_KEY>'

# List servers
claude mcp list
```

<!-- ```json
{
  "mcpServers": {
    "waha": {
      "command": "npx",
      "args": [
        "-y",
        "envmcp@0.2.1",
        "npx",
        "-y",
        "mcp-remote@0.15.1",
        "http://localhost:3002/mcp",
        "--header",
        "X-Api-Key:$WAHA_MCP_API_KEY"
      ]
    }
  }
}
``` -->
