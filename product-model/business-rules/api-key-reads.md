---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "api-key",
      "effect": "reads"
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

# Only its owner sees an API key

Each person sees only their own keys.
