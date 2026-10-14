---
{
  "domain": "api-keys",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/auth.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/migrations/006_add_api_keys.sql"
    }
  ]
}
---

# API key

A key a person creates so their automations and integrations can use the API on their behalf.

## Information kept

- **Name** — what the person called it
- **Prefix** — the first characters, shown to tell keys apart
- **Key** — the full key, shown once when it is created
- **Created at** — when it was created
- **Last used** — when it was last used

## States

### Active

Usable.

### Revoked

No longer accepted.
