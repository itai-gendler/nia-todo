---
{
  "kind": "person",
  "acts": "external",
  "relations": [
    {
      "entity": "workspace",
      "verb": "owns",
      "cardinality": "one-to-many"
    },
    {
      "entity": "project",
      "verb": "owns",
      "cardinality": "one-to-many"
    },
    {
      "entity": "project-membership",
      "verb": "holds",
      "cardinality": "one-to-many"
    },
    {
      "entity": "todo",
      "verb": "creates",
      "cardinality": "one-to-many"
    },
    {
      "entity": "comment",
      "verb": "writes",
      "cardinality": "one-to-many"
    },
    {
      "entity": "attachment",
      "verb": "uploads",
      "cardinality": "one-to-many"
    },
    {
      "entity": "reminder",
      "verb": "owns",
      "cardinality": "one-to-many"
    },
    {
      "entity": "location-reminder",
      "verb": "owns",
      "cardinality": "one-to-many"
    },
    {
      "entity": "place",
      "verb": "owns",
      "cardinality": "one-to-many"
    },
    {
      "entity": "api-key",
      "verb": "owns",
      "cardinality": "one-to-many"
    },
    {
      "entity": "push-subscription",
      "verb": "owns",
      "cardinality": "one-to-many"
    },
    {
      "entity": "password-link",
      "verb": "has",
      "cardinality": "one-to-many"
    },
    {
      "entity": "dashboard-preferences",
      "verb": "owns",
      "cardinality": "one-to-many"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/migrations/003_add_user_support.sql"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/me.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/admin.py"
    }
  ]
}
---

# User

A person with an account on the server who keeps their own workspaces, projects and todos and works in projects others share with them. Accounts are created by the administrator; the first one is created during first-run setup.

## Information kept

- **Username** — the unique name the person signs in with; only the administrator changes it
- **Display name** — the name shown to the person and to the people they share projects with, up to 80 characters
- **Email** — the address the account is reached at, unique across the server; once verified it can also be used to sign in and to be invited
- **Email verified** — whether and how the email address was confirmed: by an emailed link, by setting a password from an invitation, by first-run setup, or asserted by the administrator
- **Pending email** — a new address waiting to be confirmed through the emailed link
- **Avatar** — a square picture the person uploaded, or none
- **Language** — Automatic (the browser language) or one of the twelve languages the app ships
- **Default reminder** — how long before a deadline the automatic reminder fires, or none
- **Password** — the secret the person signs in with, chosen by the person through a password link or in settings
- **First user** — whether this is the account created during first-run setup
- **Attachment quota** — how much attachment storage the person may use; empty means the server default
- **BrainDump access** — whether the administrator lets the person use BrainDump
- **Dashboard sync** — whether the person keeps their dashboard preferences in their account rather than on each device
