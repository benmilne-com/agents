# benmilne.com — Agent Discovery

## About

Personal site and long-form archive of Ben Milne, founder of Dwolla. 66+ posts on payments, fintech, leadership, and building companies. Multilingual support for 14 languages.

## Endpoints

| Surface | URL |
|---|---|
| API | https://benmilne.com/api |
| OpenAPI | https://benmilne.com/openapi.json |
| MCP (streamable-http) | `POST https://benmilne.com/mcp` |
| MCP (SSE) | `GET https://benmilne.com/mcp/sse` |
| MCP server card | https://benmilne.com/.well-known/mcp/server-card.json |
| NLWeb /ask | `POST https://benmilne.com/ask` |
| Search (JSON) | https://benmilne.com/api/search?q={query} |
| Search (SSE) | https://benmilne.com/api/stream/search?q={query} |
| Sandbox | https://benmilne.com/sandbox |
| llms.txt | https://benmilne.com/llms.txt |
| llms-full.txt | https://benmilne.com/llms-full.txt |
| RSS | https://benmilne.com/feed.xml |
| Agent card (A2A) | https://benmilne.com/.well-known/agent-card.json |
| Agent skills | https://benmilne.com/.well-known/agent-skills/index.json |
| auth.md | https://benmilne.com/auth.md |
| Status | https://benmilne.com/status |

## Authentication

All endpoints are public and unauthenticated. No API key or token required.

## MCP Quick Start

```json
{
  "mcpServers": {
    "benmilne": {
      "url": "https://benmilne.com/mcp",
      "transport": "streamable-http"
    }
  }
}
```

## CLI

```bash
npm install -g benmilne-api
benmilne posts
benmilne search "payments"
benmilne post rate-of-change --json
```

## NLWeb /ask

```bash
curl -X POST https://benmilne.com/ask \
  -H "Content-Type: application/json" \
  -d '{"query": "What is the value layer?"}'
```

## Multilingual

14 languages supported. Add `?lang=<code>` to any content endpoint.

Codes: en, es, fr, de, pt-br, ja, zh, ko, ar, hi, it, nl, ru, tr

## Content negotiation

The same URL serves HTML, JSON, or Markdown depending on the `Accept` header.

## Sandbox

Use `https://benmilne.com/sandbox` as your base URL during development. Returns canned test data that won't change.
