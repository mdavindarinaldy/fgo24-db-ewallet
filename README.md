# E-Wallet - ERD

This project was made by Muhammad Davinda Rinaldy in Training Program held by Kodacademy to make ERD of an E-Wallet, using mermaid tool.

## Entity Relationship Diagram (ERD)

```mermaid
erDiagram
    direction LR
    users {
        int id PK
        string name
        string phone_number
    }
    user_balance {
        int id PK
        id id_users FK
        decimal balance
        timestamp created_at
    }
    transactions {
        int id PK
        date transaction_date
        decimal nominal
        string id_type_transaction FK
        string id_users FK
        string id_other_users FK
    }
    type_transactions {
        int id PK
        string type
    }
    users ||--o{ transactions : performs
    users ||--o{ transactions : receives
    users ||--o{ user_balance : has
    type_transactions ||--o{ transactions : categorizes
```
