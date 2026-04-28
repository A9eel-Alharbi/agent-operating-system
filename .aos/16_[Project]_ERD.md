# [Project Name] ERD

## Tables

### users
| Column | Type | Constraints |
|---|---|---|
| id | uuid | PK |
| email | string | unique, not null |
| password_hash | string | not null |
| created_at | timestamp | not null |

### [next table]
| Column | Type | Constraints |
|---|---|---|
| id | uuid | PK |
| user_id | uuid | FK → users.id |
[Continue for all tables]

## Indexes
- [table(column)]

## Unique Constraints
- [table(column)]
