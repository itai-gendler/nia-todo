---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "api-key",
      "effect": "changes",
      "to": "Revoked"
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "owns",
          "entity": "user"
        }
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/auth.py"
    }
  ]
}
---

# Only its owner revokes an API key

A person revokes only their own keys.
