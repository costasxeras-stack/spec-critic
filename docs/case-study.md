# Case study: Spec Critic

## The question

Specs reach refinement with the same gaps again and again: no measurable success metric, vague words like "intuitive", missing edge cases and a fixed date for an open technical question. A good engineering lead catches these in minutes, but not every PM has one on hand before the meeting. I wanted to see whether an AI reviewer could give that review in a form a PM can trust: every point tied to a real line, and nothing that looks like evidence when it is not.

## Approach

I wrote the checklist I use when I review a spec, turned the mechanical part into rules, and gave the judgement part to the model with a strict output contract. The model must quote the line each issue is about, and the app checks that quote. The live call was tested with a mocked API response, including a made-up quote, to confirm it is flagged.

## Decisions

### The visitor's own API key, plus a demo

A portfolio app with my key in it would expose the key or need a server. A server adds cost and abuse risk.

**Decision:** Call the API from the browser with the visitor's key and show a labelled demo for everyone else.

Full record: [decisions/0001-visitor-key.md](decisions/0001-visitor-key.md)

### Check every quote against the spec

Models can produce text that looks like a quote but is not in the source. A reviewer that misquotes loses trust fast.

**Decision:** Normalise spaces and quote marks, then check each quote appears in the spec. Flag any that do not, instead of hiding them.

Full record: [decisions/0002-verify-quotes.md](decisions/0002-verify-quotes.md)

### A rules-based check that runs without AI

Some checks do not need a model, and a visitor without a key should still get value.

**Decision:** Run section, vague word and metric checks instantly as the user types, separate from the AI review.

Full record: [decisions/0003-rules-before-ai.md](decisions/0003-rules-before-ai.md)

### A fixed JSON shape for the review

Free text is hard to render and impossible to check.

**Decision:** Ask for JSON in a fixed shape, extract the object from the reply, and show a clear error if the shape is wrong.

Full record: [decisions/0004-json-contract.md](decisions/0004-json-contract.md)

## What I learned as a PM

- The trust problem in AI review is provenance: tying each point to a line matters more than the wording of the advice
- A labelled demo is a product decision, not a shortcut: it sets expectations for visitors without a key
- Splitting rules from model judgement makes the AI part smaller and easier to evaluate

## Limits

- The live review has been tested with a mocked response only. A real-key test is pending
- Scores are the model's judgement and can vary between runs
- The rules check reads headings in English only

## What I would do next

1. Test the live review with my own key on [number] real specs and report the quote match rate
2. Let users mark an issue as wrong, to measure precision
3. Compare scores before and after edits to the same spec

## My role

I framed the problem, made the product calls, checked every number and wrote the conclusions. 
