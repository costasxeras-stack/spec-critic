# Changelog

All notable changes to this project. Versions follow [docs/versioning.md](docs/versioning.md).

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
