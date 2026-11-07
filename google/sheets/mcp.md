# Google Sheets MCP

## Dependencies

- [Google Cloud Platform (GCP) CLI](/gcp/README.md#cli)
- [Google Workspace (GWS) CLI](/google/workspace/README.md#cli), with `gws auth setup` completed

## Enable the MCP API

`gws auth setup` enables `sheets.googleapis.com` but not the MCP endpoint:

```sh
gcloud services enable sheetsmcp.googleapis.com --project "$(gcloud config get-value project)"
```

## Adding

```sh
# User Level
claude mcp add --transport http -s user google-sheets https://sheetsmcp.googleapis.com/mcp/v1

# List servers
claude mcp list
```

## Issues

### TBD

```log
SDK auth failed: Incompatible auth server: does not support dynamic client registration
```

```sh
CLIENT_JSON=~/.config/gws/client_secret.json
CLIENT_ID=$(jq -r '.installed.client_id' "$CLIENT_JSON")
export MCP_CLIENT_SECRET=$(jq -r '.installed.client_secret' "$CLIENT_JSON")

claude mcp remove -s user google-sheets

claude mcp add --transport http -s user google-sheets https://sheetsmcp.googleapis.com/mcp/v1 \
  --client-id "$CLIENT_ID" \
  --client-secret

claude mcp list
```
