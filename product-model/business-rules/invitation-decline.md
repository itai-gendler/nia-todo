---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "project-membership",
      "effect": "changes",
      "to": "Declined"
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

# Only the invitee declines an invitation

Declining is the invitee's answer.
