# benmilne.com

Public API for Ben Milne's essay archive. No authentication required.

## Quick start

```bash
curl https://benmilne.com/api/posts
curl -X POST https://benmilne.com/mcp -H 'Content-Type: application/json' -d '{"jsonrpc":"2.0","id":1,"method":"tools/list"}'
curl -X POST https://benmilne.com/graphql -H 'Content-Type: application/json' -d '{"query":"{ posts(first:5) { edges { node { slug title } } } }"}'
```

## Endpoints

- REST: `https://benmilne.com/api/posts`, `/api/search?q=`, `/api/site`
- GraphQL: `POST https://benmilne.com/graphql`
- MCP: `POST https://benmilne.com/mcp`
- OpenAPI: `https://benmilne.com/openapi.json`
- Full docs: `https://benmilne.com/llms-full.txt`
