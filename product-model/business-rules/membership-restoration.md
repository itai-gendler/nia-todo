---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "project-membership",
      "effect": "changes",
      "from": "Removed",
      "to": "Accepted"
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "has",
          "entity": "project"
        },
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
      "target": "api/routers/sharing.py"
    }
  ]
}
---

# Only the owner restores a removed member

Undoing a removal gives the member access again.
