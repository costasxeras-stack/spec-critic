# 0002: Check every quote against the spec

**Status:** accepted, 0.1.0

## Context

Models can produce text that looks like a quote but is not in the source. A reviewer that misquotes loses trust fast.

## Decision

Normalise spaces and quote marks, then check each quote appears in the spec. Flag any that do not, instead of hiding them.

## Tradeoff

- Slight wording differences are flagged even when the point is fair
- A reader can see at a glance which points are anchored in the text
