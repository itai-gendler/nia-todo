---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "project-membership",
      "effect": "changes",
      "to": "Pending"
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

# Only the owner invites again someone who declined, left or was removed

A new invitation to a former member or invitee is up to the owner.
