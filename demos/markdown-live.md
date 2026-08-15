---
title: Markdown and Live editing demo
type: feature-demo
status: maintained
owner: OpenGlance maintainers
last_updated: 2026-08-15
ai_snippet: "[Demo] Preview Source Live frontmatter headings lists links tasks and source-backed lines"
---

# Markdown and Live editing

This page is designed for OpenGlance screenshots and hands-on checks. Every visible sentence describes
the product rather than an unrelated sample organization.

## Three views, one source file

| Mode | Best use |
| --- | --- |
| Preview | Read rendered documents, follow links, and select source-backed context |
| Live | Make a focused edit while headings, lists, links, images, and tables stay readable |
| Source | Inspect exact Markdown, MDX, frontmatter, or structured data |

Switch modes and confirm that each view refers to this same file.

## A focused editing checklist

- [ ] Open this page in Preview and use the document outline.
- [ ] Switch to Live and edit this checklist item.
- [ ] Follow the link to the [table demo](live-table-editing.md).
- [ ] Switch to Source and inspect the frontmatter.
- [ ] Undo the practice edit before publishing.

## Portable Markdown

OpenGlance keeps ordinary content in ordinary files:

- **bold text** remains Markdown;
- *emphasis* remains Markdown;
- `inline code` remains source-readable;
- internal links remain repository-relative;
- block structure remains available to agents.

> OpenGlance is the human interface over a shared Git repository, not a second hosted copy of its
> documents.

#### Skipped heading levels stay compact

This H4 intentionally follows an H2. OpenGlance includes it one navigation depth below the parent rather
than preserving an empty H3 indentation level.

##### H5 remains one step deeper

This H5 appears one navigation depth below the H4, while the source remains ordinary portable Markdown.

## Agent-facing instruction example

```markdown
Read AGENTS.md first. Update only the requested document, preserve portable Markdown,
and return an Open in OpenGlance link for the result.
```

## Continue the tour

- [Live table editing](live-table-editing.md)
- [Image editing](image-editing.md)
- [Mermaid diagrams](mermaid-diagrams.md)
- [Agent Context and Sync](agent-context-and-sync.md)
- [MDX-lite components](mdx-lite-components.mdx)
