# Lighthouse Garden shared context repository

English | [简体中文](README.zh-CN.md)

Welcome to the shared context repository for a small, completely fictional community-garden team. It
keeps the goals, current plans, decisions, and reusable playbooks that help volunteers and AI agents
work from the same information. Git preserves the files and their history.

Nothing here is private or operational. All names, events, dates, and numbers are examples released
under CC0.

## Try it in Git Leaf

1. [Install Git Leaf](https://gitleaf.mangofuture.com/download).
2. Clone this repository:

   ```bash
   git clone https://github.com/MangoFuture1210/git-leaf-example-knowledge-base.git
   ```

3. Open the cloned folder in Git Leaf.

If Git Leaf is already installed, use
[Open in Git Leaf](https://gitleaf.mangofuture.com/open?repo=mangofuture1210%2Fgit-leaf-example-knowledge-base&path=README.md).

## One repository, several ways to use it

- **People** can open the repository in Git Leaf and start with
  [project context](context/project-context.md).
- **AI agents** can read [AGENTS.md](AGENTS.md) first, then follow its routes to the relevant context.
- **Developers and maintainers** can use their normal Git and editor tools.

Everyone works with the same ordinary files; Git Leaf is the human interface, not a second copy of the
content.

## A short tour

- [Project context and shared goals](context/project-context.md) — the entry point for the team.
- [Weekly garden routine](playbooks/weekly-garden-routine.md) — a reusable playbook.
- [Spring open day](projects/spring-open-day.md) — one project with owners and status.
- [Why Git is the source of truth](decisions/0001-git-is-the-source-of-truth.md) — a durable decision.
- [Garden overview](overview.mdx) — a structured summary with a timeline and metrics.

Try asking an external agent to read `AGENTS.md` and update one open question in the spring open-day
plan. Then return to Git Leaf, open the changed document in Preview, inspect it in **Sync**, and select a
few exact lines for **Agent Context**. You can make a focused correction in Live before publishing the
result.

## What this example intentionally avoids

- no company-specific process or professional jargon;
- no Git credentials, automation secrets, or private data;
- no arbitrary JSX or executable document scripts;
- no assumption that Git Leaf hosts the content.

The repository is the team's durable shared context and source of truth. Its knowledge documents are
one part of that context. Git Leaf is the desktop app that gives people a familiar way to read and
maintain it.
