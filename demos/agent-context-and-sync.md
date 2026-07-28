---
title: Agent Context and Sync demo
type: feature-demo
status: maintained
last_updated: 2026-07-28
ai_snippet: "[Demo] Select exact source-backed lines collect Agent Context inspect local changes and publish deliberately"
---

# Agent Context and Sync

This page provides bounded passages for testing source-backed selection and a harmless local edit for
testing Sync.

## Passage A: product boundary

Git Leaf opens a local Git repository and presents it as a readable workspace. The repository remains
the shared source of truth. Git Leaf does not upload the content or create a separate hosted copy.

Select the two sentences above and confirm that copied context includes this file path and its exact
source lines.

## Passage B: human and agent interfaces

People use Preview, Live, and Source to read, inspect, and make focused edits. Agents and developers
work directly with the same repository through Git and their normal tools.

Add this passage to Agent Context together with Passage A. The collection should preserve the source of
each excerpt.

## Harmless Sync exercise

Change the unchecked item in Live, then inspect the **Sync** view:

- [ ] Temporary local edit for the Sync demo.

Expected behavior:

1. automatic save writes the local Markdown file;
2. Sync shows this file as unpublished;
3. publishing remains an explicit action;
4. undoing the edit returns the working tree to its previous content.

Do not publish the practice edit unless you intentionally want to change the public demo.

## Link handoff

An Open in Git Leaf link identifies a GitHub repository and a repository-relative Markdown or MDX
path. Git Leaf resolves that identity to a local checkout; the hosted page does not receive the
repository contents.

Return to the [demo index](../README.md).
