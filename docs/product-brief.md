# Product brief: Spec Critic

## Problem

Specs reach refinement with the same gaps again and again: no measurable success metric, vague words like "intuitive", missing edge cases and a fixed date for an open technical question. A good engineering lead catches these in minutes, but not every PM has one on hand before the meeting. I wanted to see whether an AI reviewer could give that review in a form a PM can trust: every point tied to a real line, and nothing that looks like evidence when it is not.

## Users

- Product managers who want a spec checked before refinement
- Junior PMs learning what a reviewable spec looks like
- Hiring managers looking at how I design an AI product with guardrails

## Goals for 0.1.0

- A useful spec review in under a minute
- No claim on screen that cannot be traced to the spec
- No server and no stored keys

## Non-goals for 0.1.0

- Writing specs for the user
- Storing specs or reviews

## Success measures

| Measure | Definition | Target |
|---|---|---|
| Reviews run | Live reviews per visitor with a key | [target] |
| Quote match rate | Share of model quotes found in the spec | [target] |
| Fix adoption | Share of issues the author says they fixed, once feedback is added | [target] |
