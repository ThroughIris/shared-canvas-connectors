# Connection and privacy

- This package contains configuration for the public HTTPS endpoint at `https://sharedcanvas.ai/api/canvas-mcp/mcp`. It does not contain Shared Canvas application code, data, credentials, or a shared account.
- It uses your own Shared Canvas authorization. Your AI client manages its connection credentials. Only connect an account you intend to use with that client.
- The client can send requests that include canvas identifiers, user-supplied text and requested edits. Content returned to the AI client is subject to that client's policies. See the [Shared Canvas privacy policy](https://sharedcanvas.ai/privacy).
- The documented setup requests `account:access`, `canvases:read`, `canvases:write` and `agents:read`. Check the actual consent screen. Do not approve broader permissions unless you intend to grant them.
- Disconnect a client from **Settings → Connections → Assistant access** in Shared Canvas. Your saved canvases stay in your account.
