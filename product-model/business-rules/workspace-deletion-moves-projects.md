---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "delete-workspace"
    },
    {
      "type": "entity",
      "id": "project",
      "facts": [
        "Workspace"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/workspaces.py"
    }
  ]
}
---

# Deleting a workspace moves its projects to the default workspace

Projects of a deleted workspace move to the default workspace and its Inbox todos to the default Inbox.
