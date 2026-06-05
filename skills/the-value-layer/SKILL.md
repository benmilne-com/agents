---
name: the-value-layer
description: >-
  Retrieve metadata and download The Value Layer PDF book about internet payment infrastructure.
---

# The Value Layer — benmilne.com

Digital edition of *The Value Layer* — a free PDF book about internet payment infrastructure by Ben Milne.

## Machine-readable endpoints

- Product JSON: `GET https://benmilne.com/api/products/the-value-layer`
- x402 settings: `GET https://benmilne.com/x402/v1/settings`
- UCP manifest: `GET https://benmilne.com/.well-known/ucp`
- Landing page: `https://benmilne.com/book/the-value-layer`

## Quick start

```bash
# Get product metadata
curl https://benmilne.com/api/products/the-value-layer

# Download the PDF directly
curl -L https://benmilne.com/book/the-value-layer/download -o the-value-layer.pdf
```

## Procedural outline

1. `GET https://benmilne.com/api/products/the-value-layer` — product metadata, pricing, and download info.
2. `GET https://benmilne.com/book/the-value-layer/download` — direct PDF download.
