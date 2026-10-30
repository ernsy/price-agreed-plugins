# Price Agreed plugin for ChatGPT

The package uploaded to the OpenAI platform (Plugins, Upload new or existing
plugin) for the ChatGPT plugin directory, in the Agent Plugins format.

## What's inside

- `plugin.json`: package identity, the listing (`extensions.com.openai.interface`)
  and the reviewer test cases (`review`), which the portal imports read-only.
  The demo video URL is entered in the dashboard.
- `mcp.json`: the Price Agreed MCP server at `https://mcp.priceagreed.com/mcp/chatgpt`
  (Streamable HTTP, no authentication).
- `skills/hire-a-tradesperson`: the same skill as the other plugins.
- `assets/logo.png`: the 512 x 512 logo from `frontend/public/logo-512.png`.

## Making the ZIP

Zip the contents of this folder, not the folder itself, so `plugin.json` is at
the root of the archive:

```sh
cd plugins/chatgpt && zip -r ../../price-agreed-chatgpt.zip . -x README.md
```

Bump `version` for every new upload. Changes to the MCP tools need no new ZIP:
OpenAI rescans the server.
