---
title: README
created: 2026-08-11
tags:
  - meta
---

# my-notes

An [Obsidian](https://obsidian.md) vault — a folder of plain Markdown files,
wired to be edited both by hand in Obsidian and by [Claude Code](https://claude.com/claude-code)
from the terminal.

There is no database and no export step. Every note is a `.md` file you can read
with any text editor, which is exactly what makes agent editing possible.

## Opening it

Install Obsidian, then **Open folder as vault** and point it at this directory.
To work on it with an agent, run `claude` from this folder and ask in plain language.

## Layout

| Folder | Purpose |
|---|---|
| `inbox/` | Unsorted capture. Anything new and unfiled lands here. |
| `notes/` | The real vault. Topic folders live inside. |
| `archive/` | Superseded notes. Nothing is deleted, only moved here. |
| `attachments/` | Images, PDFs, and other binaries. |

`notes/engineering-brain` is a symlink to a separate repository that versions
itself. It is intentionally absent from this repo — clone that repo separately if
you need it.

## Conventions

- Every note opens with frontmatter carrying `title`, `created`, and `tags`.
- Internal links are `[[Wikilinks]]`, never relative paths, so renames stay intact.
- Filenames are the note title in Title Case. No dates in the name.
- Index notes (maps of content) are named `MOC — Topic.md`.
- Many small linked notes beat one long note.

The authoritative set lives in `CLAUDE.md`, which is also how the agent learns the
rules. Edit that file when the way you work changes.

## Where to start

`Start Here.md` covers the syntax worth knowing and the kinds of requests that are
tedious by hand but fast for an agent.

> [!note] Reading this on GitHub
> Wikilinks show as literal `[[text]]` and callouts as plain quotes — GitHub does
> not implement Obsidian's extensions. Open the vault in Obsidian for links,
> backlinks, and graph view.
