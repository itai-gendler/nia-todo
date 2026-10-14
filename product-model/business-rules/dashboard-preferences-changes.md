---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "dashboard-preferences",
      "effect": "changes"
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
      "target": "api/routers/me.py"
    }
  ]
}
---

# Only its owner changes dashboard preferences

Each person's dashboard is their own.
