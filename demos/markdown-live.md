---
title: Markdown and Live editing demo
type: feature-demo
status: maintained
owner: Git Leaf maintainers
last_updated: 2026-07-28
ai_snippet: "[Demo] Preview Source Live frontmatter headings lists links tasks and source-backed lines"
---

# Markdown and Live editing

This page is designed for Git Leaf screenshots and hands-on checks. Every visible sentence describes
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

Git Leaf keeps ordinary content in ordinary files:

- **bold text** remains Markdown;
- *emphasis* remains Markdown;
- `inline code` remains source-readable;
- internal links remain repository-relative;
- block structure remains available to agents.

> Git Leaf is the human interface over a shared Git repository, not a second hosted copy of its
> documents.

## Agent-facing instruction example

```markdown
Read AGENTS.md first. Update only the requested document, preserve portable Markdown,
and return an Open in Git Leaf link for the result.
```

## Continue the tour

- [Live table editing](live-table-editing.md)
- [Image editing](image-editing.md)
- [Agent Context and Sync](agent-context-and-sync.md)
- [MDX-lite components](mdx-lite-components.mdx)
