---
title: Example
created: 2026-08-12
tags:
  - meta
---

# Example

A first note, mostly to prove the vault works. The diagram below is how a note
moves through this vault.

```mermaid
graph LR
    A[Capture] --> B[inbox/]
    B --> C{Worth keeping?}
    C -->|Yes| D[notes/]
    C -->|No| E[archive/]
    D --> E
```

> [!note] Mermaid renders in reading view
> In edit mode you see the code fence; switch to reading view (`Cmd+E`) to see
> the actual diagram.
a



