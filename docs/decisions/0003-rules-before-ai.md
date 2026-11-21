# 0003: A rules-based check that runs without AI

**Status:** accepted, 0.1.0

## Context

Some checks do not need a model, and a visitor without a key should still get value.

## Decision

Run section, vague word and metric checks instantly as the user types, separate from the AI review.

## Tradeoff

- Rules are crude: a heading named differently counts as missing
- Instant, free and predictable
