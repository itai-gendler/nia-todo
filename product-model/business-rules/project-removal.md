---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "project",
      "effect": "removes"
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "owns",
          "entity": "user"
        }
      ],
      "when": [
        {
          "fact": "Inbox",
          "is": "No"
        }
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/projects.py"
    }
  ]
}
---

# Only the owner deletes a project, and never an Inbox

An Inbox cannot be deleted; any other project only by its owner.
