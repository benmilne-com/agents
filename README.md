# benmilne-com/agents

Agent discovery configuration, agent skills, and developer resources for [benmilne.com](https://benmilne.com).

## Install MCP Server

| Platform | Action |
|---|---|
| VS Code | [Add to VS Code](https://insiders.vscode.dev/redirect?url=vscode%3Amcp%2Finstall%3F%257B%2522name%2522%253A%2522benmilne%2522%252C%2522type%2522%253A%2522http%2522%252C%2522url%2522%253A%2522https%253A%252F%252Fbenmilne.com%252Fmcp%2522%257D) |
| Cursor | [Add to Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=benmilne&config=eyJ1cmwiOiJodHRwczovL2Jlbm1pbG5lLmNvbS9tY3AifQ==) |
| Claude | `claude mcp add --transport http benmilne https://benmilne.com/mcp` |
| Any MCP client | `POST https://benmilne.com/mcp` (Streamable HTTP JSON-RPC) |

## Agent Skills

Install skills for AI coding agents:

```bash
npx skills add benmilne-com/agents
```

| Skill | Description |
|---|---|
| [mcp-api](skills/mcp-api/SKILL.md) | Query and search benmilne.com content via MCP JSON-RPC tools |
| [content-search](skills/content-search/SKILL.md) | Full-text search across 69 published essays |
| [the-value-layer](skills/the-value-layer/SKILL.md) | Retrieve and download The Value Layer PDF book |

## Quick links

- [MCP server docs](https://benmilne.com/mcp/docs)
- [Agent discovery guide](AGENTS.md)
- [API documentation](https://benmilne.com/api)
- [API llms.txt](https://benmilne.com/api/llms.txt)
- [OpenAPI spec](https://benmilne.com/openapi.json)
- [GraphQL API](https://benmilne.com/graphql)
- [MCP server card](https://benmilne.com/.well-known/mcp/server-card.json)
- [A2A agent card](https://benmilne.com/.well-known/agent.json)
- [Agent skills index](https://benmilne.com/.well-known/agent-skills/index.json)
- [npm package](https://www.npmjs.com/package/benmilne-api)
- [PyPI package](https://pypi.org/project/benmilne-api/)

## CLI

```bash
# Node.js
npm install -g benmilne-api
benmilne search "payments"

# Python
pip install benmilne-api
benmilne-api search "stablecoins"
```

See `AGENTS.md` for full endpoint documentation.

## License

MIT
