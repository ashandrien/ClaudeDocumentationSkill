# Docstrings

Follow the project's linter settings for required docstrings. Where they aren't required, treat
docstrings as opt-in and skip them on obvious internal functions.

Docstrings are worth writing for:
- Public APIs.
- Complex behavior.
- Important assumptions.
- Non-obvious parameters.
- Business rules.
- External integration requirements.

Keep them short. Leave out what the function name, parameter types, or implementation already make
obvious.

A docstring describes the function as it is. Don't record the conversation, session, review or request
that produced it (no "added per feedback", "now also handles…", "changed from…"). See
`code-comments.md`.
