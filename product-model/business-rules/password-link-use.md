---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "password-link",
      "effect": "changes",
      "to": "Used"
    }
  ],
  "permits": [
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
      "target": "api/routers/password_setup.py"
    }
  ]
}
---

# Only the person a password link is for uses it

Using a link sets the password of the account it was made for.
