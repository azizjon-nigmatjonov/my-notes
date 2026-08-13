```mermaid
graph LR
    A[Capture] --> B[inbox/]
    B --> C{Worth keeping?}
    C -->|Yes| D[notes/]
    C -->|No| E[archive/]
    D --> E
```