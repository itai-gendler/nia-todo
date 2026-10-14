---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "project-membership",
      "effect": "changes",
      "from": "Pending",
      "to": "Accepted"
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "holds",
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

# Only the invitee accepts an invitation

Nobody accepts an invitation on someone else's behalf.
