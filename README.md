# benmilne-com/agents

Agent discovery configuration, agent skills, and developer resources for [benmilne.com](https://benmilne.com).

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

- [Agent discovery guide](AGENTS.md)
- [API documentation](https://benmilne.com/api)
- [OpenAPI spec](https://benmilne.com/openapi.json)
- [MCP server card](https://benmilne.com/.well-known/mcp/server-card.json)
- [Agent skills index](https://benmilne.com/.well-known/agent-skills/index.json)
- [CLI package](https://www.npmjs.com/package/benmilne-api)

## CLI

```bash
npm install -g benmilne-api
benmilne search "payments"
```

See `AGENTS.md` for full endpoint documentation.

## License

MIT
