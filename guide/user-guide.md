---
title: Git Leaf user guide demo
type: user-guide-demo
status: maintained
canonical: false
source_repository: MangoFuture1210/git-leaf
source_path: docs/user-guide.md
source_revision: eda6624
last_updated: 2026-08-04
ai_snippet: "[Guide] Try Git Leaf reading, editing, Mermaid, MDX-lite, Agent Context, Sync, and links in one public repository"
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

When several repositories are open, use the repository button beside the current name or press
`Command+O` on macOS and `Ctrl+O` on Windows. The centered panel can search the stable repository list;
while it is open, `Command+1` through `Command+9` (`Ctrl+1` through `Ctrl+9` on Windows) select the
numbered visible repositories, and `Command+0` or `Ctrl+0` opens another local repository. A row can be
removed from Git Leaf without deleting its local files. The worktree selector remains a separate control
from the repository panel: when multiple worktrees exist, it replaces the repeated standalone repository
name in the sidebar header while the repository button stays beside it.

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

- click a cell to edit only that cell's source, then drag from the active editor into a neighboring cell
  to extend the selection;
- drag horizontally, vertically, or diagonally to select the rectangle between two cells;
- use the formatting toolbar fixed above the table for bold, italic, strikethrough, foreground color,
  or text-only highlight;
- align every column touched by the selection; clearing text formatting keeps alignment unchanged;
- open either fixed color palette only when needed, then close the toolbar with its close button or
  Escape;
- select two or more cells vertically in one column to reveal the column drag handle and move the whole
  column.

Preview stays read-only. The saved source remains a native pipe table using standard Markdown,
separator-row alignment, and controlled inline styles that can still be opened in Obsidian.

Open [Live table editing](../demos/live-table-editing.md) for the complete scenario.

## 6. Work with images

Live can turn a Markdown image into a controlled HTML image line when an explicit width, alignment, or
caption is needed. The source remains inspectable and only safe image attributes are retained.

Open [Image editing](../demos/image-editing.md), switch to Live, and select the Git Leaf icon.

## 7. Explore a Mermaid architecture diagram

Standard fenced Mermaid remains portable Markdown. Git Leaf renders it locally in Preview and in an
inactive Live block, while preserving the exact source and its line range.

Open [Mermaid diagrams](../demos/mermaid-diagrams.md). In the dense flowchart, confirm that **Smart
view** presents the complete topology vertically without a node selector or synthetic local graph.
Turn Smart view off and on and confirm that every node and relationship remains present. Use **Fit
width**, zoom, drag, and `</>` to inspect the exact source. Compare that complete reading view with the
explicit `block-beta` map; then switch to Live and confirm that both blocks remain visual outside their
source lines.

## 8. Keep structured data readable to agents

Git Leaf MDX-lite accepts a bounded component set whose data remains ordinary CSV, TSV, JSON, or
Markdown text. `Chart` and `DataTable` can also reference a repository-local `.dataset.json` contract
beside a maintained full CSV or JSON data file. The report chooses an inclusive date range and readers
can select only views supported by its declared source granularity without changing the source data.
Daily sources offer day, week, month, and natural-quarter views; weekly sources offer only week.

Git Leaf does not execute arbitrary JSX, imports, scripts, or event handlers. Dataset aggregation uses
only the typed fields and explicit rollups declared by the manifest.

In Live, click a rendered component to keep it visual and open one compact toolbar. `DataTable` exposes
its common table settings, `Chart` exposes type and value labels, and `DecisionBox` exposes status. Every
component uses one `</>` entry for its source, whether its data is inline or external. Close the toolbar
with its close button, Escape, or by selecting another object.

Dataset day, week, month, and quarter buttons remain reader controls inside the rendered component. They
do not open the editing toolbar and never write MDX.

Open [MDX-lite components](../demos/mdx-lite-components.mdx) to inspect DataTable, Timeline, Chart,
DecisionBox, MetricGrid, and FlowDiagram in Preview, Live, and Source. In the external dataset section,
switch the same daily source among the four time intervals. Then open the dedicated
[external dataset report](../demos/external-dataset-report.mdx) to inspect the three-file contract,
date range, typed filter, expected quarterly result, and the weekly source's single safe view.

## 9. Give exact context to an agent

Source-backed line selection makes a passage useful outside the app without losing its repository path
and source lines. Several passages can be collected into Agent Context before handing them to an
external agent.

Open [Agent Context and Sync](../demos/agent-context-and-sync.md) and follow its bounded selection
exercise.

## 10. Inspect and publish changes deliberately

Automatic save writes the local file. Sync shows unpublished files and remote state. Publishing remains
an explicit Git action; Git Leaf does not silently publish unfinished work or rewrite diverged history.

The Agent Context and Sync demo includes a harmless edit you can make and then revert.

## 11. Use the right boundary

Git Leaf is for reading, inspecting, and making focused edits to repository context. Use a full editor
for broad code changes, a Git conflict tool for complex merges, and an external agent for larger
repository tasks.

Return to the [demo index](../README.md) or open the
[canonical Git Leaf documentation](https://github.com/MangoFuture1210/git-leaf/tree/main/docs).
