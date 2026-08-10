---
title: Start Here
created: 2026-08-10
tags:
  - meta
---

# Start Here

This vault is wired up to work with Claude Code. Open a terminal in this folder,
run `claude`, and ask for what you want in plain language.

> [!tip] The one thing to understand
> A vault is just a folder of plain `.md` files. That is why Claude can work on it
> at all — there is no API and no export step. Your notes are ==files==, and Claude
> is good at files.

## What to ask for

Things that are tedious by hand and fast for an agent:

- `File everything in inbox/ under the right topic and tag it`
- `Build MOC — Machine Learning linking every note that mentions a model`
- `Read https://example.com/article and save a clean summary to inbox/`
- `Find notes where I've said contradictory things`
- `Normalize the frontmatter across every note in notes/`

## Syntax worth knowing

| You write | You get |
|---|---|
| `[[Note Name]]` | A link, and an edge in the graph view |
| `[[Note Name\|other text]]` | Same link, different label |
| `![[image.png\|400]]` | Embedded image, 400px wide |
| `#topic/subtopic` | A nested tag |
| `==text==` | Highlight |
| `%%hidden%%` | A comment only you see in edit mode |

> [!note]- Callouts fold
> Start a callout with `> [!note]`. Add `-` after the type to make it collapsed
> by default, like this one. Types include `tip`, `warning`, `question`, `example`,
> `danger`, and `todo`.

## Conventions in this vault

The full set lives in `CLAUDE.md` at the vault root — that file is how Claude
learns your rules. Edit it whenever you change how you work, and Claude follows
along on the next session.

- [ ] Open Obsidian and point it at this folder
- [ ] Enable the CLI in Settings → General → Command line interface
- [ ] Write one real note and link it from here
