# [Project Name] Security

## Authentication
- Hashing: [e.g., "Argon2id"]
- Access token: [e.g., "30 min"]
- Refresh token: [e.g., "7 days, rotation"]

## Encryption
- [What]: [e.g., "AES-256-GCM"]

## Rate Limiting
| Endpoint | Limit |
|---|---|
| Auth | [e.g., "5/min"] |
| API | [e.g., "60/min"] |

## Env Variables
| Variable | Purpose |
|---|---|
| DATABASE_URL | DB connection |
| JWT_SECRET_KEY | Token signing |
