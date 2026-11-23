# 0005: Editor's desk design and demo on load

**Status:** Accepted · 23 November 2026

## Context

Version 0.1.0 shared one visual template with the other portfolio apps, and a first visit showed an empty review panel until the visitor loaded the sample and pressed a button. Most visitors never reach the output.

## Decision

Design the page as an editor's desk. The spec is a white page set in Source Serif 4. The overall score is a red-pen grade circled on the review, and each issue shows its quote in highlighter yellow, the way an editor marks a draft. Colours: desk grey, graphite, red pen and highlighter yellow. Interface type: Schibsted Grotesk.

On first load, the page fills in the sample spec and shows the stored demo review. The banner above the grade still says it is a stored demo review and not a live model call. A visitor who wants a live review switches to "AI review with my key" as before.

## Consequences

- The output is visible on arrival, so the page shows what the product does without a click.
- The demo review is pre-written. The label stays visible above the grade so it is not mistaken for a live run.
