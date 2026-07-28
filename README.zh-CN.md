# Lighthouse Garden 团队上下文仓库

[English](README.md) | 简体中文

这是一个完全虚构的小型社区花园团队的共享上下文仓库。其中保存共同目标、当前计划、决定和可复用的操作手册，
让志愿者和 AI Agent 使用同一份信息；Git 负责保存文件及其历史。

这里没有任何私密或真实运营资料。所有姓名、活动、日期和数字都是示例，并以 CC0 发布。

## 在 Git Leaf 中体验

1. [安装 Git Leaf](https://gitleaf.mangofuture.com/download?lang=zh-CN)。
2. 克隆此仓库：

   ```bash
   git clone https://github.com/MangoFuture1210/git-leaf-example-knowledge-base.git
   ```

3. 在 Git Leaf 中打开克隆后的目录。

如果已经安装 Git Leaf，也可以直接
[在 Git Leaf 中打开](https://gitleaf.mangofuture.com/open?repo=mangofuture1210%2Fgit-leaf-example-knowledge-base&path=README.zh-CN.md)。

## 一个仓库，多种使用方式

- **普通团队成员**可以在 Git Leaf 中打开仓库，从[项目上下文](context/project-context.md)开始阅读。
- **AI Agent** 先读取 [AGENTS.md](AGENTS.md)，再按其中的路径找到相关上下文。
- **开发者和维护者**可以继续使用熟悉的 Git 和编辑器工具。

所有人使用同一组普通文件；Git Leaf 是面向人的界面，不会再复制一套内容。

## 快速浏览

- [项目上下文与共同目标](context/project-context.md)：团队的内容入口。
- [每周花园例行事项](playbooks/weekly-garden-routine.md)：可复用的操作手册。
- [春季开放日](projects/spring-open-day.md)：带负责人和状态的小项目。
- [为什么以 Git 为事实源](decisions/0001-git-is-the-source-of-truth.md)：一项长期决定。
- [花园概览](overview.mdx)：包含时间线和指标的结构化摘要。

可以先让外部 Agent 读取 `AGENTS.md`，更新春季开放日计划中的一个待定问题。然后回到 Git Leaf，在
Preview 中打开改过的文档，通过 **Sync** 检查变化，再选择几行准确内容加入 **Agent Context**；如果只需
小幅修正，也可以直接在 Live 中完成后再发布。

仓库是团队持久的共享上下文和事实源，知识文档是其中一部分；Git Leaf 是让人以熟悉方式阅读和维护它的桌面
App。
