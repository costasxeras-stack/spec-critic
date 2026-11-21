# 0001: The visitor's own API key, plus a demo

**Status:** accepted, 0.1.0

## Context

A portfolio app with my key in it would expose the key or need a server. A server adds cost and abuse risk.

## Decision

Call the API from the browser with the visitor's key and show a labelled demo for everyone else.

## Tradeoff

- Most visitors will only see the demo
- No server, no stored keys, no bill for me
