# Changelog

All notable changes to this project. Versions follow [docs/versioning.md](docs/versioning.md).

## [0.2.0] - 2026-11-23

### Changed
- New design: an editor's desk. The spec sits on a white page in a serif, the overall score is a red-pen grade circled on the page, and every quoted line in the issues is highlighted in yellow.
- The page opens with the sample spec and the stored demo review already shown, labelled as a demo, so a visitor sees the output without clicking.
- Own look for this app: desk grey, graphite, red pen, highlighter yellow, Schibsted Grotesk and Source Serif 4.

### Added
- Decision record: editor's desk design and demo on load.

The rules check, the AI review and the quote check are unchanged.

## [0.1.0] - 2026-11-21

First release.

### Added
- Instant check in plain JavaScript: required sections, vague words, numbers in success metrics, list items
- AI review through the Claude Messages API with the visitor's own key and a choice of model
- Structured output: six scores with reasons, issues with severity, section, exact quote, problem and fix, questions and a rewrite
- Quote verification: every quote from the model is checked against the spec and flagged if it is not found
- Demo mode with a stored, hand-written review of a sample spec, clearly labelled as not a live call
- Issue filter by severity and copy as Markdown
- Key handling: the key goes only to Anthropic's API and is kept in the tab only if the visitor asks
