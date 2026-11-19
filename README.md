# Shared Canvas connectors

Connect Codex or Claude Code to your own [Shared Canvas](https://sharedcanvas.ai/) account to find, read and edit canvases you already have permission to use.

**Public beta.** This is the Shared Canvas GitHub marketplace, not a listing in an official Codex or Claude directory. You'll need a Shared Canvas account. If you're new, create one on the [Shared Canvas homepage](https://sharedcanvas.ai/) and confirm your email before connecting.

## Codex CLI

Tested with macOS Codex CLI **0.169.1**. Run:

```sh
codex plugin marketplace add ThroughIris/shared-canvas-connectors
codex plugin add shared-canvas@shared-canvas
codex mcp login sharedcanvas --oauth-client-registration cimd --scopes account:access,canvases:read,canvases:write,agents:read
```

Use the explicit scope command above. An unscoped login can request more permissions. Review the browser consent screen before approving.

## Claude Code

Tested with macOS Claude Code **2.1.322**. Run:

```sh
claude plugin install shared-canvas --marketplace ThroughIris/shared-canvas-connectors
```

In Claude Code, open `/mcp`, select Shared Canvas and sign in to your account. Confirm the server is from the plugin, not a separate manual MCP entry for the same URL. If one is already configured, leave it in place and test the plugin in a fresh profile.

## Test the connection

Ask your assistant to list the Shared Canvas canvases you can access. For a write test, ask it to create a private scratch canvas in one of your own agents, then open the canvas in Shared Canvas to see the change.

Both clients request four permissions: account access, canvas read and write, and listing owned agents. The connector can edit canvases where you have write access. Installation alone does not sign you in or give access to someone else's private content. Never paste your password, access token or API key into chat or a config file.

To stop access, open **Settings → Connections → Assistant access** in Shared Canvas and choose **Disconnect** for the client. This leaves your saved canvases in place. When you want to reconnect, sign in and review the permissions again.

See [connection and privacy details](docs/PRIVACY.md), the [Shared Canvas privacy policy](https://sharedcanvas.ai/privacy), and [terms of use](https://sharedcanvas.ai/terms).
