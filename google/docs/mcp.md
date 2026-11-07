# Google Docs MCP

## Dependencies

- [Google Cloud Platform (GCP) CLI](/gcp/README.md#cli)
- [Google Workspace (GWS) CLI](/google/workspace/README.md#cli), with `gws auth setup` completed

## Enable the MCP API

`gws auth setup` enables `docs.googleapis.com` but not the MCP endpoint:

```sh
gcloud services enable docsmcp.googleapis.com --project "$(gcloud config get-value project)"
```

## Adding

```sh
# User Level
claude mcp add --transport http -s user google-docs https://docsmcp.googleapis.com/mcp/v1

# List servers
claude mcp list
```

<!-- ```json
{
  "mcpServers": {
    "google-docs": {
      "type": "http",
      "url": "https://docsmcp.googleapis.com/mcp/v1"
    }
  }
}
``` -->

<!-- {
  "mcpServers": {
    "google-docs": {
      "serverUrl": "https://docsmcp.googleapis.com/mcp/v1",
      "oauth": {
        "clientId": "OAUTH_CLIENT_ID",
        "clientSecret": "OAUTH_CLIENT_SECRET"
      }
    }
  }
} -->

## Issues

### TBD

```log
SDK auth failed: Incompatible auth server: does not support dynamic client registration
```

```sh
CLIENT_JSON=~/.config/gws/client_secret.json
CLIENT_ID=$(jq -r '.installed.client_id' "$CLIENT_JSON")
export MCP_CLIENT_SECRET=$(jq -r '.installed.client_secret' "$CLIENT_JSON")

claude mcp remove -s user google-docs

claude mcp add --transport http -s user google-docs https://docsmcp.googleapis.com/mcp/v1 \
  --client-id "$CLIENT_ID" \
  --client-secret

claude mcp list
```
