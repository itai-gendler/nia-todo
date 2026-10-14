---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "share-project"
    },
    {
      "type": "entity",
      "id": "project-membership",
      "effect": "creates"
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

# An invitation goes to another person who is not already in the project

The owner cannot invite themselves, nor someone who already has access or a pending invitation.
