# Adding content

This file isn't part of the published site (it's excluded in `_config.yml`) — it's just a quick reference for adding new entries.

## New blog post

Add a file to `_posts/` named `YYYY-MM-DD-some-title.md`:

```
---
layout: post
title: Your post title
---

Body text goes here, in Markdown.
```

It'll show up automatically on the homepage and on [/contents/](/contents/).

## New "Plant and Animal Life and Random Finds" entry

Add a file to `_finds/` — the filename doesn't need a date prefix, e.g. `_finds/tree-frog.md`:

```
---
title: Tree frog on the window screen
date: 2026-08-19
image: /images/finds/tree-frog.jpg
---

A short description, and whatever you were thinking at the time.
```

- `date` controls sort order (newest first) — always include it.
- `image` is optional. Put the photo in `images/finds/` (create the folder if it doesn't exist) and point to it with that same path.
- You don't need to add `layout: find` — it's applied automatically to everything in `_finds/`.

It'll show up automatically in the gallery at [/finds/](/finds/) and in its own section on [/contents/](/contents/).
