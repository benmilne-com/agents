---
name: mcp-api
description: Query and search benmilne.com content via MCP REST paths and JSON-RPC tools.
---

# MCP API — benmilne.com

Machine-readable interfaces for autonomous agents integrating with Ben Milne's published archive.

## Capabilities
- Paginated posts: `GET https://benmilne.com/mcp/v1/posts`
- Single post: `GET https://benmilne.com/mcp/v1/post/{id}`
- Search: `GET https://benmilne.com/mcp/v1/search?query=`
- MCP JSON-RPC: `POST https://benmilne.com/mcp` (`initialize`, `tools/list`, `tools/call`)

## Tools

The MCP server exposes 3 tools via `tools/list`:

- **list_posts** — Browse, filter, and paginate all published posts. Supports optional `category` and `tag` filters.
- **get_post** — Retrieve a single post with full HTML content by numeric ID.
- **search_posts** — Full-text search across all published posts by keyword.

## Quick start

```bash
# List tools
curl -X POST https://benmilne.com/mcp \
  -H 'Content-Type: application/json' \
  -d '{"jsonrpc":"2.0","id":1,"method":"tools/list"}'

# Search for posts about stablecoins
curl -X POST https://benmilne.com/mcp \
  -H 'Content-Type: application/json' \
  -d '{"jsonrpc":"2.0","id":2,"method":"tools/call","params":{"name":"search_posts","arguments":{"query":"stablecoin"}}}'
```

## Notes
Attribution is included in JSON envelopes. Prefer JSON for agents; use `Accept: text/markdown` on essay routes for prose.
