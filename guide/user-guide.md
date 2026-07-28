---
title: Git Leaf user guide demo
type: user-guide-demo
status: maintained
canonical: false
source_repository: MangoFuture1210/git-leaf
source_path: docs/user-guide.md
source_revision: 58fe9b4
last_updated: 2026-07-28
ai_snippet: "[Guide] Try Git Leaf reading, editing, MDX-lite, Agent Context, Sync, and links in one public repository"
---

# Git Leaf user guide demo

[简体中文](user-guide.zh-CN.md) | English

This page is a runnable companion to the canonical
[Git Leaf user guide](https://github.com/MangoFuture1210/git-leaf/blob/main/docs/user-guide.md).
It summarizes the main path and links to files that exercise each interaction.

## 1. Open an ordinary Git repository

Git Leaf opens an existing local Git repository. It does not upload the repository or create a second
copy of its documents. The directory tree, Git history, and source files remain available to every
other Git tool.

Use this repository for the tour so every visible document describes the product you are using.

## 2. Read in Preview

Preview is the read-only view for following links and reading rendered Markdown or MDX. Source-backed
line numbers remain available, and the document outline follows the headings on the page.

Open [Markdown and Live](../demos/markdown-live.md), then try:

1. selecting a heading from the outline;
2. following an internal document link;
3. selecting exact source-backed lines;
4. using Command-click on macOS or Ctrl-click on Windows to open a second tab.

## 3. Make a focused change in Live

Live keeps common document structure readable while editing the original Markdown or MDX source. It is
suited to small corrections, lists, links, images, and native Markdown tables.

Open [Markdown and Live](../demos/markdown-live.md), switch to Live, and edit one checklist item. The
file is saved automatically to the working tree; it is not shared until it is committed and pushed.

## 4. Inspect exact source

Source shows exact Markdown, MDX, frontmatter, and structured component data beside the rendered
document. Use it when syntax matters or when you want to inspect an agent-authored change precisely.

Switch between Preview, Live, and Source on the same page. They are three views of one file, not three
document formats.

## 5. Edit a native Markdown table

In Live, a native pipe table remains rendered:

- click a cell to edit only that cell's source;
- drag horizontally, vertically, or diagonally to select the rectangle between two cells;
- use the floating palette to color every selected cell;
- select a complete column to reveal the handle used to move that column.

Preview stays read-only. The saved source remains a native pipe table with a controlled inline color
span that can still be opened in Obsidian.

Open [Live table editing](../demos/live-table-editing.md) for the complete scenario.

## 6. Work with images

Live can turn a Markdown image into a controlled HTML image line when an explicit width, alignment, or
caption is needed. The source remains inspectable and only safe image attributes are retained.

Open [Image editing](../demos/image-editing.md), switch to Live, and select the Git Leaf icon.

## 7. Keep structured data readable to agents

Git Leaf MDX-lite accepts a bounded component set whose data remains ordinary CSV, TSV, JSON, or
Markdown text. It does not execute arbitrary JSX, imports, scripts, or event handlers.

Open [MDX-lite components](../demos/mdx-lite-components.mdx) to inspect DataTable, Timeline, Chart,
DecisionBox, MetricGrid, and FlowDiagram in Preview and Source.

## 8. Give exact context to an agent

Source-backed line selection makes a passage useful outside the app without losing its repository path
and source lines. Several passages can be collected into Agent Context before handing them to an
external agent.

Open [Agent Context and Sync](../demos/agent-context-and-sync.md) and follow its bounded selection
exercise.

## 9. Inspect and publish changes deliberately

Automatic save writes the local file. Sync shows unpublished files and remote state. Publishing remains
an explicit Git action; Git Leaf does not silently publish unfinished work or rewrite diverged history.

The Agent Context and Sync demo includes a harmless edit you can make and then revert.

## 10. Use the right boundary

Git Leaf is for reading, inspecting, and making focused edits to repository context. Use a full editor
for broad code changes, a Git conflict tool for complex merges, and an external agent for larger
repository tasks.

Return to the [demo index](../README.md) or open the
[canonical Git Leaf documentation](https://github.com/MangoFuture1210/git-leaf/tree/main/docs).
