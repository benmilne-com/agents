---
name: content-search
description: Full-text search across all published posts on benmilne.com.
---

# Full-text search — benmilne.com

Search 69 published essays on payments, fintech, stablecoin infrastructure, and protocol thinking.

## Usage

```bash
# REST API
curl 'https://benmilne.com/api/search?q=payment+network'

# MCP REST path
curl 'https://benmilne.com/mcp/v1/search?query=payment+network'

# MCP JSON-RPC
curl -X POST https://benmilne.com/mcp \
  -H 'Content-Type: application/json' \
  -d '{"jsonrpc":"2.0","id":1,"method":"tools/call","params":{"name":"search_posts","arguments":{"query":"payment network"}}}'

# SSE streaming
curl 'https://benmilne.com/api/stream/search?q=payment+network'

# NLWeb natural language
curl -X POST https://benmilne.com/ask \
  -H 'Content-Type: application/json' \
  -d '{"query":"What has Ben Milne written about stablecoin regulation?"}'
```

## Response format

Results are ranked by relevance and include title, date, URL, and excerpt for each matching post.
