# my-notes — Obsidian vault

This directory is an Obsidian vault. Every `.md` file here is a note that a human
reads and edits inside Obsidian, not source code.

## Skills

The `obsidian-*`, `json-canvas`, and `defuddle` skills in `.claude/skills/` are
installed from [kepano/obsidian-skills](https://github.com/kepano/obsidian-skills).
Use them:

- Writing or editing any `.md` file here → `obsidian-markdown`
- Creating a `.base` database view → `obsidian-bases`
- Creating a `.canvas` visual map → `json-canvas`
- Reading a web page to save into the vault → `defuddle` (not WebFetch)
- Driving a running Obsidian instance from the shell → `obsidian-cli`

## Folder layout

| Folder | Purpose |
|---|---|
| `inbox/` | Unsorted capture. Anything new and unfiled lands here. |
| `notes/` | The real vault. Topic folders live inside. |
| `archive/` | Superseded notes. Nothing is ever deleted, only moved here. |
| `attachments/` | Images, PDFs, and other binaries. |
| `vaults/` | Additional Obsidian vaults. New vaults go here, one folder each. |

`notes/engineering-brain/` is a **symlink** to `../../aziz-engineering-brain`, a
separate git repo with its own GitHub remote. Obsidian reads it like any other
folder, but this vault's git ignores it — commit changes there from its own
directory, not from here. `dashboard-brain` depends on that repo's original path,
so do not move or rename it.

## Conventions

- Every note starts with frontmatter carrying `title`, `created` (`YYYY-MM-DD`), and `tags`.
- Link notes with `[[Wikilinks]]`, never relative paths — Obsidian tracks renames through them.
- Use `[text](url)` only for external URLs.
- Filenames are the note title in Title Case, spaces allowed, no dates in the name.
- Prefer many small linked notes over one long note.
- Index notes (maps of content) are named `MOC — Topic.md`.

## Rules

- Never edit anything in `.obsidian/` — that is app configuration.
- Never create a new vault outside `vaults/`. Every new vault Claude opens or
  creates lives in `vaults/<Vault Name>/` — never at the repo root, never
  elsewhere on disk.
- Never delete a note. Move it to `archive/` instead.
- Never rewrite a note's prose wholesale unless asked; these are the user's own words.
- Commit before any operation that touches more than a handful of notes.
