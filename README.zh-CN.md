# Git Leaf 使用指南 Demo

[English](README.md) | 简体中文

这是 [Git Leaf](https://github.com/MangoFuture1210/git-leaf) 使用指南的公开、可操作配套仓库。仓库里的
文字直接介绍 Git Leaf，因此当这些页面出现在产品截图、上手演示或人工验收中时，画面里的内容本身也有意义。

Git Leaf 是本地 Git 仓库面向人的界面。人可以在 Git Leaf 中阅读、检查和做小范围修改；Agent 与开发者
仍然直接使用同一组 Git 文件和自己熟悉的工具。

## 在 Git Leaf 中体验

1. [安装 Git Leaf](https://gitleaf.mangofuture.com/download?lang=zh-CN)。
2. 克隆此仓库：

   ```bash
   git clone https://github.com/MangoFuture1210/git-leaf-example-knowledge-base.git
   ```

3. 在 Git Leaf 中打开克隆后的目录。

如果已经安装 Git Leaf，也可以直接
[在 Git Leaf 中打开](https://gitleaf.mangofuture.com/open?repo=mangofuture1210%2Fgit-leaf-example-knowledge-base&path=README.zh-CN.md)。

## 从使用指南开始

- [Git Leaf 使用指南 Demo](guide/user-guide.zh-CN.md)：一条简洁的产品体验路线，链接会带你进入对应的
  可操作示例。
- [English user guide demo](guide/user-guide.md)：英文版本。

## 主要功能 Demo

| Demo | 可以体验什么 |
| --- | --- |
| [Markdown 与 Live](demos/markdown-live.md) | Preview、目录、Source、Live、Frontmatter、链接、列表和任务 |
| [Live 表格编辑](demos/live-table-editing.md) | 单元格局部源码、矩形选区、文字颜色与列移动 |
| [图片编辑](demos/image-editing.md) | Markdown 图片与 Live 图片工具栏 |
| [Agent Context 与 Sync](demos/agent-context-and-sync.md) | 带来源的行选择、小范围修改与未发布改动检查 |
| [MDX-lite 组件](demos/mdx-lite-components.mdx) | DataTable、Timeline、Chart、DecisionBox、MetricGrid 与 FlowDiagram |

## 维护方式

产品事实和正式使用文档仍以 Git Leaf 源码仓库为准。这里的改写页面会记录上游来源与版本；稳定的用户可见
功能、操作流程或截图场景变化时，应同步检查此仓库。私密资料、可执行的任意 MDX，以及只用于回归测试的边界
样例不会放进公开 Demo。

除明确标记的 MDX-lite Demo 外，其余示例保持与 Obsidian，以及支持普通 Markdown、GFM 表格和安全内联
HTML 的工具兼容。

## 许可

本仓库与 Git Leaf 一样，采用 [Apache License 2.0](LICENSE)。
