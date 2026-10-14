---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "create-api-key"
    },
    {
      "type": "entity",
      "id": "api-key",
      "facts": [
        "Key"
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

# An API key is shown in full only when it is created

Afterwards only its prefix identifies it.
