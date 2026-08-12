# AGENTS.md - OpenPeek User Guide Demo

This public repository is the runnable companion to OpenPeek's user guide. People open it in OpenPeek
to learn the product and exercise its main document interactions; agents and maintainers edit the same
ordinary Git files directly.

## Read before changing anything

1. Start with `README.md` and its Simplified Chinese counterpart.
2. Read `guide/user-guide.md` for the guided product tour.
3. Open the relevant file under `demos/` before changing a feature example.
4. Verify current product facts in the upstream
   [`MangoFuture1210/openpeek`](https://github.com/MangoFuture1210/openpeek) repository.

## Authority and synchronization

- The OpenPeek repository owns product behavior, architecture, release policy, and the canonical user
  guide. This repository is a public demo, not a second source of product truth.
- When a stable user-visible OpenPeek capability, workflow, or screenshot scenario changes, review the
  matching page here in the same maintenance cycle.
- Copied or adapted material must record its upstream source path and revision in frontmatter.
- Keep this repository useful on its own, but link to upstream technical documentation instead of
  duplicating architecture or release policy.

## Demo rules

- Every visible example must be about OpenPeek, its repository workflow, or its documentation. Do not
  add an unrelated fictional story merely to fill a screenshot.
- Cover stable primary capabilities. Keep security probes, unsupported syntax, stress fixtures, and
  regression-only edge cases in the OpenPeek product repository.
- Markdown examples should remain portable to Obsidian and other CommonMark or GFM tools. MDX-lite
  examples are the explicit OpenPeek extension.
- Preserve frontmatter, relative links, accessible image alt text, and source-readable sample data.
- Do not add personal data, credentials, private operational material, or claims not verified against
  the current upstream repository.
