---
title: Live Markdown table editing demo
type: feature-demo
status: maintained
source_repository: MangoFuture1210/openpeek
source_path: docs/user-guide.md
source_revision: c8e0eab
last_updated: 2026-07-28
ai_snippet: "[Demo] Native Markdown table cell editing rectangular formatting column alignment and reorder in Live"
---

# Live Markdown table editing

Use this page in **Live**. Preview is intentionally read-only, and Source always exposes the exact pipe
table written to disk.

## 1. Select and format a rectangular range

Drag horizontally, vertically, or diagonally across adjacent cells. OpenPeek selects the complete
rectangle bounded by the first and last cell. The toolbar stays above the table instead of following
the selection. Use it to apply bold, italic, strikethrough, foreground color, or text-only highlight
across the range. The two color palettes expand only when opened.

| OpenPeek surface | Project role | Review signal | Recommended mode |
| :--- | :--- | :---: | :---: |
| README | **Product entry point** | <span style="color: #16a34a; background-color: #16a34a33;">Current</span> | Preview |
| User guide | _End-user workflow_ | <span style="color: #2563eb; background-color: #2563eb33;">Reference</span> | Preview or Live |
| Feature demo | Hands-on acceptance | <span style="color: #d97706; background-color: #d9770633;">Review</span> | Live |
| Old screenshot | ~~Superseded behavior~~ | <span style="color: #dc2626; background-color: #dc262633;">Replace</span> | Source |

## 2. Edit one cell without exposing the whole table

Click the `Focused edit` cell. Only that cell shows its raw Markdown source; the rest of the table stays
rendered. While the editor is still active, start dragging inside it and cross into a neighboring cell.
The editor commits and the gesture becomes a rectangular table selection.

| Interaction | Expected result | Scope |
| --- | --- | --- |
| Click one cell | Focused edit | Current cell |
| Drag from the active cell | Rectangular selection | Bounded range |
| Choose a text format | Portable Markdown or controlled inline style | Entire selected cells |
| Choose left, center, or right alignment | Native separator-row colons | Every selected column |
| Clear text formatting | Plain cell content; alignment remains | Entire selected cells |
| Close the toolbar or press Escape | Clear the selection | Current interaction |

## 3. Align selected columns

Select one cell or a rectangle spanning several columns, then use the three alignment buttons. Every
column touched by the selection changes alignment, even when only some body rows are selected. OpenPeek
updates only the native Markdown separator row.

| Document surface | Source owner | Priority | Status |
| :--- | :--- | ---: | :---: |
| Product behavior | OpenPeek source | 1 | Current |
| User workflow | User guide | 2 | Maintained |
| Public demonstration | This repository | 3 | Maintained |
| Regression edge cases | Product tests | 4 | Separate |

## 4. Move a column from a vertical range

Select any vertical range of at least two cells within one column. The column drag handle appears
without requiring the complete column to be selected. Drag it left or right; the header, alignment
separator, and every body cell move together.

## 5. Inspect controlled colors and highlights

These cells are already stored with the same fixed palette written by the Live toolbar.

| Signal | OpenPeek meaning | Foreground | Text highlight |
| --- | --- | --- | --- |
| Positive | Successful or improving | <span style="color: #16a34a;">Ready</span> | <span style="background-color: #16a34a33;">Ready</span> |
| Risk | Blocked or unsafe | <span style="color: #dc2626;">Needs attention</span> | <span style="background-color: #dc262633;">Needs attention</span> |
| Warning | Review soon | <span style="color: #d97706;">Watch</span> | <span style="background-color: #d9770633;">Watch</span> |
| Information | Neutral context | <span style="color: #2563eb;">Reference</span> | <span style="background-color: #2563eb33;">Reference</span> |
| Neutral | Secondary detail | <span style="color: #64748b;">Not applicable</span> | <span style="background-color: #64748b33;">Not applicable</span> |

## 6. Preserve normal Markdown boundaries

| Case | Rendered content | Source remains |
| --- | --- | --- |
| Bold | **Git remains authoritative** | `**Git remains authoritative**` |
| Italic | _Review before publishing_ | `_Review before publishing_` |
| Strikethrough | ~~Old screenshot~~ | `~~Old screenshot~~` |
| Escaped pipe | Preview \| Live | `Preview \| Live` |
| Inline code | `Preview|Live` | `` `Preview|Live` `` |

OpenPeek writes native pipe-table syntax, standard Markdown emphasis, separator-row alignment, and
narrowly controlled inline color spans. Highlight affects only the text background, not the complete
cell. There is no font-size control. This keeps the Markdown table editable in Obsidian; MDX-lite
remains a separate OpenPeek extension.
