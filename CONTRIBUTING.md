# Contributing to Vibe Coding 101

Thank you for helping build the most useful open-source handbook on
AI-powered software development. This document explains how to
contribute effectively.

## Ground Rules

1. **No placeholders.** Never submit a page with "Coming soon," empty
   sections, or lorem ipsum. If a page isn't ready, don't open the PR yet.
2. **No pure link lists.** Every addition must explain *why* and *how*,
   not just point somewhere else.
3. **Write like documentation, not a blog post.** Clear, direct,
   example-driven. Model your writing on Stripe Docs or MDN.
4. **Cross-link.** Every new page should link to at least one related
   page, and be linked from at least one index (its folder's `README.md`
   and the relevant table in the root `README.md`).
5. **Keep structure consistent.** Follow the [page template](#page-template)
   below for docs pages.

## Ways to Contribute

| Contribution type | Where it goes |
|---|---|
| New concept/topic page | `docs/<topic-folder>/` |
| New reusable prompt | `prompts/<category>/` |
| New quick reference | `cheat-sheets/<category>/` |
| New project blueprint | `guides/blueprints/<project-type>/` |
| New tool entry | `awesome-tools/` |
| Fix, typo, clarification | anywhere |
| Diagram | `diagrams/`, referenced from the relevant doc |

## Before You Open a PR

1. **Search first.** Check `docs/`, `prompts/`, and `awesome-tools/` for
   existing coverage of your topic to avoid duplicates. If you're
   extending an existing page, edit it rather than creating a near-copy.
2. **Follow naming conventions:**
   - Folders: `kebab-case`, numeric prefix for ordered `docs/` topics
     (e.g. `07-prompt-engineering`).
   - Files: `README.md` for a folder's index page; otherwise
     `kebab-case.md`.
3. **Update navigation.** Add a link to your new page in:
   - the folder's own `README.md` (or create one if the folder didn't
     have an index),
   - the root `README.md` table if you added a new top-level section.
4. **Run a spell/lint pass.** Use any Markdown linter (e.g.
   `markdownlint`) before submitting.

## Page Template

Every page under `docs/` should include these sections, in this order:

```markdown
# Page Title

## Introduction
## Why It Matters
## First Principles
## How It Works
## Architecture / Diagram (Mermaid)
## Real Examples
## Best Practices
## Common Mistakes
## Prompt Templates (if applicable)
## Summary
## Related Pages
```

Not every section needs to be long — but none should be skipped or left
as a stub. If a section genuinely doesn't apply, say so in one line
rather than omitting it silently.

## Style Guide

- Use second person ("you") for instructional content.
- Use fenced code blocks with language tags for all code.
- Use tables for comparisons (tools, trade-offs, options).
- Use Mermaid for anything spatial or sequential (architecture, flows,
  state machines).
- Prefer short paragraphs and bullet lists over long prose blocks.
- Cite sources for factual claims about specific tools, pricing, or
  benchmarks, and note the date you verified them (tool pricing and
  capabilities change quickly).

## Review Process

1. Open a PR against `main`.
2. A maintainer checks it against the rules above (no placeholders,
   correct structure, cross-linked, no duplication).
3. Once approved, it's merged and indexed.

## Reporting Issues

Use GitHub Issues for:
- Outdated information (tool pricing, model names, deprecated APIs)
- Broken links
- Missing topics you'd like to see covered

## Code of Conduct

By participating, you agree to abide by our
[Code of Conduct](CODE_OF_CONDUCT.md).
