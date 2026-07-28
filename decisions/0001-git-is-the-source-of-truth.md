---
title: Keep Git as the source of truth
status: accepted
date: 2026-03-02
---

# Keep Git as the source of truth

## Decision

The files in this repository are the team's authoritative shared context. Git Leaf is the human
interface used to read and maintain them; automation and AI agents work with the same files through Git.

## Why

- The content remains portable Markdown and MDX.
- Changes have a reviewable history.
- People and tools do not need separate copies of the context.
- The repository can be opened with other editors if needed.

## Consequences

- A change is not shared until it is committed and pushed.
- Private repositories still depend on each participant’s existing Git access.
- The app must not hide conflicts or rewrite diverged history automatically.
