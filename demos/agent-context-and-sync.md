---
title: Agent Context and Sync demo
type: feature-demo
status: maintained
source_repository: MangoFuture1210/git-leaf
source_path: docs/user-guide.md
source_revision: ed188c5
last_updated: 2026-08-11
ai_snippet: "[Demo] Select exact source-backed lines collect Agent Context locate document edits inspect local changes and publish deliberately"
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

In Live, check the item and temporarily remove the word `local`, then return to Preview:

- [ ] Temporary local edit for the Sync demo.

Expected behavior:

1. automatic save writes the local Markdown file;
2. the edited line uses a warm highlight, and **Harmless Sync exercise** uses that color across the full
   document-navigation row while still jumping here;
3. **Show deletions** starts off; turning it on shows `local` as underlined read-only text and changes the
   gutter to committed/current line-number columns;
4. opening another document and returning restores the same cues;
5. Sync shows this file as unpublished, while publishing remains an explicit action;
6. undoing both edits returns the working tree to its previous content and clears the cues.

An edit before the first visible navigation heading would use the synthetic **Document start** row. The
in-document cues are intentionally lighter than a standard Git diff and do not stage or discard files.

Do not publish the practice edit unless you intentionally want to change the public demo.

## Link handoff

An Open in Git Leaf link identifies a GitHub repository and a repository-relative Markdown or MDX
path. Git Leaf resolves that identity to a local checkout; the hosted page does not receive the
repository contents.

Return to the [demo index](../README.md).
