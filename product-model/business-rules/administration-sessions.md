---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "sign-in-to-administration"
    },
    {
      "type": "capability",
      "id": "sign-out-of-administration"
    },
    {
      "type": "capability",
      "id": "change-admin-password"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/services/auth.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/admin.py"
    }
  ]
}
---

# Administration sessions last one day

An administration sign-in lasts at most a day; signing out, or changing the admin password, ends every administration session.
