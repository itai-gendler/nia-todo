---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "project-membership",
      "effect": "creates"
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

# Only the owner invites people to a project

Sharing a project is up to its owner.
