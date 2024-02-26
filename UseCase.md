---
mermaid: true
---

### Content Review and Ratting 

<div class="mermaid">
%% Code for flowchart below
graph TB
    sq[Square shape] --> ci((Circle shape))

    subgraph A subgraph2
        od>Odd shape]-- Two line<br>edge comment --> ro
        di{Diamond with <br/> line break} -.-> ro(Rounded<br>square<br>shape)
        di==>ro2(Rounded square shape)
    end

    %% Notice that no text in shape are added here instead that is appended further down
    e --> od3>Really long text with linebreak<br>in an Odd shape]

    %% Comments after double percent signs
    e((Inner / circle<br>and some odd <br>special characters)) --> f(,.?!+-*ز)

    cyr[Cyrillic]-->cyr2((Circle shape Начало));

     classDef green fill:#9f6,stroke:#333,stroke-width:2px;
     classDef orange fill:#f96,stroke:#333,stroke-width:4px;
     class sq,e green
     class di orange
</div>


## Flow Chart

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


## Mind mapping

``` mermaid
mindmap
root((Content))
        Reviews
            User
            Like
                User
            Dislike
                User
            Mark helpful
                User
            Reply
                User
                Reply
                    User
```

## Entity Relationship Diagram


```mermaid
erDiagram
    USER {
        UserId INT
    }

    CONTENT {
        ContentId INT
    }

    REVIEW {
        ReviewId INT
    }

    LIKE {
        LikeId INT
    }

    DISLIKE {
        DislikeId INT
    }

    MARK_HELPFUL {
        MarkHelpfulId INT
    }

    REPLY {
        ReplyId INT
    }
    CONTENT ||--o{ REVIEW : "Add Review"
    USER ||--o{ REVIEW : "Post Reviews"
    REVIEW ||--o{ LIKE : "Like"
    REVIEW ||--o{ DISLIKE : "Dislike"
    REVIEW ||--o{ MARK_HELPFUL : "Mark helpful"
    REVIEW ||--o{ REPLY : "Reply"
    LIKE ||--o{ USER : "UserId"
    DISLIKE ||--o{ USER : "UserId"
    MARK_HELPFUL ||--o{ USER : "UserId"
    REPLY ||--o{ USER : "UserId"
```

