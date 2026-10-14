---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "user",
      "effect": "changes",
      "facts": [
        "Username",
        "Attachment quota",
        "BrainDump access"
      ]
    }
  ],
  "permits": [
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
      "target": "api/routers/admin.py"
    }
  ]
}
---

# Only the administrator changes a username, attachment quota or BrainDump access

People cannot change their own username, storage quota or BrainDump access.
