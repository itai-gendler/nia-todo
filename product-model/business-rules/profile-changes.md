---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "user",
      "effect": "changes",
      "facts": [
        "Display name",
        "Email",
        "Pending email",
        "Email verified"
      ]
    }
  ],
  "permits": [
    {
      "self": true
    },
    {
      "actors": [
        "administrator"
      ]
    }
  ],
  "references": [
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

# A person and the administrator change the display name and email

Both the person and the administrator may change the display name and the email address of an account.
