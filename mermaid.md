``` mermaid
flowchart LR
    A[Content] -->|Post Reviews| B(Reviews)
    B-->|Like| D[LIKE]
    B -->|Dislike| E[Dislike]
    B -->|Mark helpfull| F[Mark helpfull]
    B -->|Reply| G[Reply]
    G -->|Reply| H[Reply]
    B-->|UserId| U[User] 
    D-->|UserId| U[User] 
    F-->|UserId| U[User]
    E-->|UserId| U[User]
    G-->|UserId| U[User]
    H-->|UserId| U[User]
```
