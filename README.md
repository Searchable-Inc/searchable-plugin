# Searchable

Connect your AI coding agent to [Searchable](https://www.searchable.com): see how your brand appears in AI answers (ChatGPT, Claude, Gemini, Perplexity, Copilot and more), which sources AI models cite, your share of voice against competitors, site health, AI traffic, and content opportunities.

This plugin contains no code. It registers Searchable's hosted MCP server:

```text
https://app.searchable.com/api/mcp-server/mcp
```

## Requirements

- A Searchable account with access to at least one project.
- A client that supports remote MCP servers over Streamable HTTP with OAuth.

## Install

| Client | How |
| --- | --- |
| Cursor and Grok Bot | Install **Searchable** from the [Cursor Marketplace](https://cursor.com/marketplace) (in Grok Bot, under **Plugins**), or use the one-click button on [docs.searchable.com/integrations/mcp](https://docs.searchable.com/integrations/mcp). |
| Claude Code | `/plugin marketplace add Searchable-Inc/searchable-plugin`, then `/plugin install searchable@searchable` |
| Codex | `codex mcp add searchable --url https://app.searchable.com/api/mcp-server/mcp` |
| Gemini CLI | `gemini extensions install https://github.com/Searchable-Inc/searchable-plugin` |
| Agent Plugins clients | Install from this repository; the root `plugin.json` and `mcp.json` follow [Agent Plugins 1.0](https://agent-plugins.org). |
| Any other MCP client | Add the server URL above as a remote (Streamable HTTP) server and sign in when prompted. Per-client steps: [docs.searchable.com/integrations/mcp](https://docs.searchable.com/integrations/mcp). |

## Sign in

No API key is needed. The first time your agent calls a Searchable tool, your client opens a browser window to sign in to Searchable and approve access (OAuth 2.1). You choose which projects the connection can see. To disconnect, log out of the server in your client's MCP settings.

## Network and credentials

The plugin connects only to `app.searchable.com`: the MCP server above and its OAuth endpoints. It reads no environment variables, files or local credentials, and runs no commands. The only credential is the OAuth token your client receives when you sign in, which your client stores.

## What you can ask

- "List my Searchable projects."
- "How visible is my brand in AI answers this month, by platform?"
- "Which sources do AI models cite most for my topics?"
- "Compare my share of voice with my top competitors."

Full tool reference: [docs.searchable.com/integrations/mcp](https://docs.searchable.com/integrations/mcp).

## Privacy and terms

Use of Searchable through this plugin is governed by the [Searchable Terms](https://www.searchable.com/terms) and [Privacy Policy](https://www.searchable.com/privacy).

## Support

Email [support@searchable.com](mailto:support@searchable.com), or see [docs.searchable.com](https://docs.searchable.com).

## License

MIT. See [LICENSE](LICENSE).
