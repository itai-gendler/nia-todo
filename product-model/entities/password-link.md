---
{
  "domain": "users",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/password_setup.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/migrations/014_add_password_setup_tokens.sql"
    }
  ]
}
---

# Password link

A one-time link that lets a person choose a password: an invitation for a new account, or a reset for an existing one.

## Information kept

- **Purpose** — Invitation or Reset
- **Expires at** — when it stops working, per the password link validity
- **Requested by** — the administrator or the person themselves

## States

### Active

Usable until it expires.

### Used

A password was set with it.

### Replaced

A newer link of the same purpose superseded it.
