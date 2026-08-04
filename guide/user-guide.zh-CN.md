---
title: Git Leaf 使用指南 Demo
type: user-guide-demo
status: maintained
canonical: false
source_repository: MangoFuture1210/git-leaf
source_path: docs/user-guide.zh-CN.md
source_revision: 14d8ed0
last_updated: 2026-08-04
ai_snippet: "[使用指南] 在一个公开仓库中体验 Git Leaf 阅读、编辑、Mermaid、MDX-lite、Agent Context、Sync 与链接"
---

# Git Leaf 使用指南 Demo

[English](user-guide.md) | 简体中文

这份文档是正式 [Git Leaf 用户手册](https://github.com/MangoFuture1210/git-leaf/blob/main/docs/user-guide.zh-CN.md)
的可操作配套版本。它把主要使用路线压缩成一页，并链接到可以直接体验相应交互的文件。

## 1. 打开一个普通 Git 仓库

Git Leaf 直接打开已经存在于本机的 Git 仓库，不会上传仓库，也不会再复制一套文档。目录、Git 历史和源文件
仍然可以由其他 Git 工具、编辑器与 Agent 使用。

本仓库里的内容直接介绍 Git Leaf，因此演示和截图中出现的文字也属于项目上下文。

## 2. 在 Preview 中阅读

Preview 用于只读浏览渲染后的 Markdown 或 MDX。文档仍保留来源行号，右侧目录会跟随页面标题。

打开 [Markdown 与 Live](../demos/markdown-live.md)，依次尝试：

1. 从文档目录跳到一个标题；
2. 打开内部文档链接；
3. 选择几行带来源的准确内容；
4. 在 macOS 使用 Command-click、在 Windows 使用 Ctrl-click 打开第二个 Tab。

## 3. 在 Live 中做小范围修改

Live 在直接编辑原始 Markdown／MDX 的同时，让常见文档结构保持易读。它适合小幅修正、列表、链接、图片和
原生 Markdown 表格。

打开 [Markdown 与 Live](../demos/markdown-live.md)，切换到 Live，修改一个清单项。文件会自动保存到本地
工作区，但提交并推送以前不会被共享。

## 4. 在 Source 中检查准确源码

Source 同时显示准确的 Markdown、MDX、Frontmatter 和结构化组件数据。语法本身很重要，或者需要仔细检查
Agent 写入的内容时，使用 Source。

在同一个页面切换 Preview、Live 与 Source。它们是同一个文件的三种视图，不是三套文档格式。

## 5. 编辑原生 Markdown 表格

在 Live 中，原生管道表格会保持渲染状态：

- 单击单元格，只编辑这个单元格的源码；即使仍在编辑，也可以从编辑框拖入相邻单元格扩大选区；
- 横向、纵向或斜向拖动，选择起点与终点围成的矩形；
- 使用固定在表格上方的格式工具栏设置粗体、斜体、删除线、前景色或文字后方的高亮色；
- 对齐选区涉及的整列；清除文字格式时保留列对齐；
- 两个固定色板只在需要时展开，工具栏可通过关闭按钮或 Esc 关闭；
- 在同一列纵向选中至少两个单元格后，使用列拖动把手移动整列。

Preview 始终只读。保存后的内容仍然是原生管道表格、标准 Markdown、分隔行对齐与受控内联样式，可以继续
在 Obsidian 中打开。

完整场景见 [Live 表格编辑](../demos/live-table-editing.md)。

## 6. 处理图片

当图片需要明确宽度、对齐或说明文字时，Live 可以把 Markdown 图片转换为受控的 HTML 图片行。源码仍然
可以检查，并且只保留安全的图片属性。

打开 [图片编辑](../demos/image-editing.md)，切换到 Live，然后选择 Git Leaf 图标。

## 7. 阅读 Mermaid 架构图

标准 Mermaid 围栏仍是可移植的 Markdown。Git Leaf 在 Preview 和 Live 的非活动区块中本地渲染，同时
保留完全相同的源码和行范围。

打开 [Mermaid 图](../demos/mermaid-diagrams.md)。在复杂 flowchart 中，确认“智能阅读”会从一个节点及其
直接关系开始；切换到另一个节点，再选择“全部节点”恢复所有节点和关系，然后关闭并重新打开“智能阅读”。
继续尝试“适应宽度”、缩放、拖动画布，并用 `</>` 检查准确源码。把这个按拓扑阅读的视图与明确指定行列和
留白的 `block-beta` 图比较；随后切换到 Live，确认光标不在源码行内时仍显示图形。

## 8. Agent 读数据，人看结构化视觉

Git Leaf MDX-lite 只接受有限的组件集合，组件数据仍然是普通 CSV、TSV、JSON 或 Markdown 文本。`Chart`
和 `DataTable` 还可以引用仓库内的 `.dataset.json` 数据契约，以及旁边长期维护的全量 CSV 或 JSON 数据文件。
报表指定包含首尾日期的区间，读者只能选择源数据粒度可靠支持的视图：日数据支持日、周、月和自然季度，
周数据只支持周；切换视图不会改动源数据。

Git Leaf 不会执行任意 JSX、import、脚本或事件处理器。数据集聚合只使用清单里明确声明的字段类型和汇总规则。

在 Live 中，单击已渲染的组件会保持视觉呈现，并打开一个紧凑工具栏。`DataTable` 提供常用表格设置，
`Chart` 提供类型和数值标签，`DecisionBox` 提供状态。无论数据在文档内还是来自外部，每个组件都只通过
一个 `</>` 入口进入源码。关闭按钮、Esc 或选择其他对象都能关闭工具栏。

数据集的日、周、月、季度按钮仍是组件内部的阅读控件。它们不会打开编辑工具栏，也不会写入 MDX。

打开 [MDX-lite 组件](../demos/mdx-lite-components.mdx)，在 Preview、Live 与 Source 中检查 DataTable、
Timeline、Chart、DecisionBox、MetricGrid 和 FlowDiagram；在外部数据集一节，把同一份日数据切换到四种
时间粒度。然后打开独立的 [外部数据集报表](../demos/external-dataset-report.mdx)，检查三文件契约、日期区间、
带类型的筛选条件、预期季度结果，以及周数据源唯一可靠的周视图。

## 9. 把准确上下文交给 Agent

带来源的行选择让离开 App 的内容仍然保留仓库路径和源码行号。还可以把多个片段整理成 Agent Context，再
交给外部 Agent。

打开 [Agent Context 与 Sync](../demos/agent-context-and-sync.md)，完成其中限定范围的选择练习。

## 10. 有意识地检查和发布改动

自动保存只负责写入本地文件。Sync 显示尚未发布的文件和远端状态；发布始终是明确的 Git 操作。Git Leaf
不会静默发布未完成内容，也不会自动重写已经分叉的历史。

Agent Context 与 Sync Demo 提供了一个可以修改、随后撤销的无害练习。

## 11. 保持工具边界

Git Leaf 适合阅读、检查和小范围编辑仓库上下文。大范围代码修改应使用完整编辑器；复杂冲突使用 Git 合并
工具；更大的仓库任务交给外部 Agent。

返回 [Demo 首页](../README.zh-CN.md)，或查看
[Git Leaf 正式文档](https://github.com/MangoFuture1210/git-leaf/tree/main/docs)。
