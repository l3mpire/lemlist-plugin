# lemlist plugin

Official lemlist plugin for AI assistants and coding agents. It connects your assistant to the hosted lemlist MCP server:

```
https://app.lemlist.com/mcp
```

With it, your assistant can list your campaigns and their stats, create campaigns with email and LinkedIn sequences, add and search leads, search the lemlist B2B people database, and check the deliverability of your sending domains.

This repository only holds the plugin manifests. The MCP server is run by lemlist; there is nothing to build or host.

## Sign-in

The server uses OAuth 2.1 (dynamic client registration and PKCE). On first use your client opens a lemlist sign-in page, and you pick the lemlist team to connect on the consent screen. Any lemlist account works, including the free trial. Enrichment and people database searches use your team's credits. An API key can be used instead of OAuth: see the setup guide below.

## Install

| Client | How |
|---|---|
| Claude Code | `/plugin marketplace add l3mpire/lemlist-plugin` then `/plugin install lemlist@lemlist` |
| Gemini CLI | `gemini extensions install https://github.com/l3mpire/lemlist-plugin` |
| Grok Build | `grok plugin install l3mpire/lemlist-plugin` |
| Kiro | [![Add to Kiro](https://kiro.dev/images/add-to-kiro.svg)](https://kiro.dev/launch/mcp/add?name=lemlist&config=%7B%22url%22%3A%22https%3A%2F%2Fapp.lemlist.com%2Fmcp%22%2C%22disabled%22%3Afalse%2C%22autoApprove%22%3A%5B%5D%7D) |
| Cursor | `.cursor-plugin/plugin.json` |
| Any MCP client | add a remote (Streamable HTTP) server with the URL `https://app.lemlist.com/mcp` |

## Manifests

- `plugin.json` and `mcp.json`: [Agent Plugins](https://agent-plugins.org) manifest (GitHub Copilot)
- `.claude-plugin/`: Claude Code plugin and marketplace
- `.cursor-plugin/plugin.json`: Cursor
- `.grok-plugin/`: Grok
- `gemini-extension.json`: Gemini CLI

## Links

- Setup guide: https://help.lemlist.com/en/articles/13728466-set-up-the-lemlist-mcp-server-in-your-llm-client-oauth-or-api-key
- Official MCP Registry entry: `io.github.l3mpire/lemlist`
- lemlist: https://www.lemlist.com
- Privacy policy: https://www.lemlist.com/legal/privacy-policy
- Support: https://help.lemlist.com

## License

MIT
