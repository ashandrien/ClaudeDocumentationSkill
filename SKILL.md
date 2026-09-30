---
name: documentation
description: How to write documentation. Load before 1) writing or editing code comments, 2) writing or editing docstrings, 3) writing a PR description, 4) writing a PR review comment, 5) writing or editing a Markdown doc (README, architecture notes, CLAUDE.md, skills), or 6) deciding whether a doc should exist at all.
---

# Documentation

Everything written here is read by engineers at every level of experience, who likely haven't seen the
conversation or ticket it came from. Each kind of writing has its own file. Read the one that matches
the task, plus `prose.md` where it says so. Don't load the others.

## Which file to read

| You are writing | Read |
| --- | --- |
| A code comment | `code-comments.md` |
| A docstring | `docstrings.md` |
| A PR description, an artifact, or any other explanation for someone else | `prose.md` |
| A PR review comment | `pr-comments.md`, then `prose.md` (the section on acknowledging good work) |
| A Markdown doc, `CLAUDE.md`, or a skill; or deciding whether a doc should exist | `markdown-docs.md`, then `prose.md` |

If the task fits none of these, use `prose.md`.

## Rules that apply to all of them

- Write about where things stand. Leave out the conversation, session, ticket thread or review that led
  to the change.
- Use plain words.
