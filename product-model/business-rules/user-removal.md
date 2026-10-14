---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "user",
      "effect": "removes"
    }
  ],
  "permits": [
    {
      "actors": [
        "administrator"
      ],
      "when": [
        {
          "fact": "First user",
          "is": "No"
        }
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/admin.py"
    }
  ]
}
---

# Only the administrator deletes accounts, and never the first one

The account created during first-run setup cannot be deleted.
