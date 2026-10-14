---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "project",
      "effect": "changes",
      "facts": [
        "Workspace"
      ]
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

# Only the owner moves a project to another workspace, and never an Inbox

Each Inbox stays in the workspace it belongs to.
