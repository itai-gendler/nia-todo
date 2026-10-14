---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "password-link",
      "effect": "changes",
      "to": "Replaced"
    }
  ],
  "permits": [
    {
      "actors": [
        "administrator"
      ]
    },
    {
      "related": [
        {
          "verb": "has",
          "entity": "user"
        }
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/admin.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/password_setup.py"
    }
  ]
}
---

# A password link is replaced by the administrator or by its person asking for a new one

A newer link of the same purpose supersedes the earlier one.
