# Documarium connector

<img src=".claude-plugin/icon.png" alt="" width="64" height="64">

A docs site you run by asking Claude. Say what to change, check the preview, and your live site updates. No editor to open.

- **Start from what you already have.** A repo, docs online, your product's web page or a file: Claude drafts the whole site and hands you a preview link to keep or throw away, before you need an account.
- **Draft, approve and publish from the chat.** Ask Claude to draft the change, check the preview, say yes, publish. No merge button in another app.
- **One prompt makes your whole docs site multilingual.** Ask Claude for Spanish and it drafts every page in Spanish. You check them before they go live, and Documarium adds no AI meter.

Write for free. Pay when you publish.

This repository holds the public listing files for the Documarium connector. The server itself is hosted at `https://mcp.documarium.com`; there is nothing to install or run from here.

## Use it

- **Claude (web, desktop, mobile):** add the connector by URL: `https://mcp.documarium.com`. Setup guide: [docs.documarium.com](https://docs.documarium.com/getting-started/installation/?utm_source=github&utm_medium=readme&utm_campaign=C002&utm_content=DIR-2026W43-006).
- **Claude Code:** `/plugin install documarium --marketplace azatarm-prog/documarium-connector`, or `claude mcp add --transport http documarium https://mcp.documarium.com`.
- **Gemini CLI:** `gemini extensions install https://github.com/azatarm-prog/documarium-connector`.
- **Any MCP client:** the server speaks streamable HTTP with OAuth (dynamic client registration).

## What's here

| File | For |
|---|---|
| `server.json` | The official MCP Registry entry (`com.documarium/documarium`) |
| `.claude-plugin/plugin.json`, `.mcp.json`, `skills/` | The Claude Code plugin |
| `gemini-extension.json` | The Gemini CLI extension |
| `.github/workflows/publish.yml` | Publishes to the MCP Registry on a `v*` tag |

Website: [documarium.com](https://documarium.com/?utm_source=github&utm_medium=readme&utm_campaign=C002&utm_content=DIR-2026W43-006) · Privacy: [docs.documarium.com/policies/privacy](https://docs.documarium.com/policies/privacy/?utm_source=github&utm_medium=readme&utm_campaign=C002&utm_content=DIR-2026W43-006) · Support: support@documarium.com

Documarium is an independent product. It is not made by or affiliated with Anthropic; Claude is a trademark of Anthropic, PBC.

Licensed under the MIT License.
