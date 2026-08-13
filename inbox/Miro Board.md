---
title: Miro Board
created: 2026-08-12
tags:
  - tools
  - embed
---

# Miro Board

Live embed of the board. Switch to ==reading view== (`Cmd+E`) to see it — raw HTML
stays as text while you are editing.

<iframe
  width="768"
  height="432"
  src="https://miro.com/app/live-embed/YOUR_BOARD_ID/"
  style="border: none;"
  allowfullscreen
  title="Miro board"></iframe>

> [!warning] Replace `YOUR_BOARD_ID`
> The URL above is still the placeholder, so the frame will load an error page
> until it is swapped for a real board.

## Getting the real URL

In Miro, open the board and use **Share → Embed**. Copy the `src` value from the
snippet it gives you and paste it in above. The real one carries query parameters
after the ID and looks roughly like:

```
https://miro.com/app/live-embed/uXjVK4dGh2s=/?moveToViewport=-331,-462,1500,1000&embedId=123456789012
```

The board also has to be shared as **Anyone with the link** — a private board
renders as a login wall inside the frame.

## Making it fill the note width

Swap the fixed `width="768"` for a style rule if the frame should track the pane:

```html
<iframe
  style="width: 100%; aspect-ratio: 16 / 9; border: none;"
  src="https://miro.com/app/live-embed/YOUR_BOARD_ID/"
  allowfullscreen
  title="Miro board"></iframe>
```

> [!note]- Why this is HTML and not `![[...]]`
> Obsidian's embed syntax only reaches files inside the vault. Anything live from
> the web needs a real `<iframe>`, which Obsidian renders in reading view. The
> same pattern works for YouTube, Figma, and Google Docs.
