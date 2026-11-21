# 0004: A fixed JSON shape for the review

**Status:** accepted, 0.1.0

## Context

Free text is hard to render and impossible to check.

## Decision

Ask for JSON in a fixed shape, extract the object from the reply, and show a clear error if the shape is wrong.

## Tradeoff

- A small share of replies may fail to parse and need a retry
- Scores, filters and quote checks all depend on structure
