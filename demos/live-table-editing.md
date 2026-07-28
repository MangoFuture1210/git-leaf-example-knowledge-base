---
title: Live Markdown table editing demo
type: feature-demo
status: maintained
source_repository: MangoFuture1210/git-leaf
source_path: docs/user-guide.md
source_revision: 58fe9b4
last_updated: 2026-07-28
ai_snippet: "[Demo] Native Markdown table cell editing rectangular selection text color and column reorder in Live"
---

# Live Markdown table editing

Use this page in **Live**. Preview is intentionally read-only, and Source always exposes the exact pipe
table written to disk.

## 1. Select and color a rectangular range

Drag horizontally, vertically, or diagonally across adjacent cells. Git Leaf selects the complete
rectangle bounded by the first and last cell. Choose a color from the floating toolbar to apply it to
every selected cell.

| Surface | Primary purpose | Portability | Recommended mode |
| --- | --- | --- | --- |
| README | Product entry point | CommonMark | <span style="color: #dc2626;">Preview</span> |
| User guide | End-user workflow | CommonMark | <span style="color: #dc2626;">Preview or Live</span> |
| Feature demo | Hands-on acceptance | GFM table | Live |
| MDX-lite demo | Structured visual data | Git Leaf extension | Preview or Source |

## 2. Edit one cell without exposing the whole table

Click the `Focused edit` cell. Only that cell shows its raw Markdown source; the rest of the table stays
rendered.

| Interaction | Expected result | Scope |
| --- | --- | --- |
| Click one cell | Focused edit | Current cell |
| Drag across cells | Rectangular selection | Bounded range |
| Choose a color | Controlled inline span | Entire selected cells |
| Press Escape | Clear or cancel | Current interaction |

## 3. Move a complete column

Select a column from its header through the last body cell. A small handle appears above the column.
Drag the handle left or right; the header, alignment separator, and every body cell move together.

| Field | Source owner | Alignment | Status |
| :--- | :--- | ---: | :---: |
| Product behavior | Git Leaf source | 1 | Current |
| User workflow | User guide | 2 | Maintained |
| Public demonstration | This repository | 3 | Maintained |
| Regression edge cases | Product tests | 4 | Separate |

## 4. Inspect controlled colors

These cells are already stored with the same fixed palette written by the Live toolbar.

| Signal | Meaning | Demo value |
| --- | --- | --- |
| Positive | Successful or improving | <span style="color: #16a34a;">Ready</span> |
| Risk | Blocked or unsafe | <span style="color: #dc2626;">Needs attention</span> |
| Warning | Review soon | <span style="color: #d97706;">Watch</span> |
| Information | Neutral context | <span style="color: #2563eb;">Reference</span> |
| Neutral | Secondary detail | <span style="color: #64748b;">Not applicable</span> |

## 5. Preserve normal Markdown boundaries

| Case | Rendered content | Source remains |
| --- | --- | --- |
| Emphasis | **Git remains authoritative** | `**Git remains authoritative**` |
| Escaped pipe | Preview \| Live | `Preview \| Live` |
| Inline code | `Preview|Live` | `` `Preview|Live` `` |

Git Leaf writes native pipe-table syntax plus narrowly controlled inline color spans. This keeps the
Markdown table editable in Obsidian; MDX-lite remains a separate Git Leaf extension.
