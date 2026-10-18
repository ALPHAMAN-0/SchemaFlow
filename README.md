# SchemaFlow
SchemaFlow helps developers write database schema code and instantly visualize it as an ER diagram. I want to build it because large database designs are hard to understand from code alone, especially when many tables and relationships are involved.

## Architecture / How it Works

```mermaid
erDiagram
    USER ||--o{ ORDER : places
    ORDER ||--|{ ITEM : contains
    USER {
        int id PK
        string name
        string email
    }
    ORDER {
        int id PK
        date created_at
        int user_id FK
    }
    ITEM {
        int id PK
        string title
        int order_id FK
    }
```

