---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "workspace"
    },
    {
      "type": "entity",
      "id": "project",
      "facts": [
        "Inbox"
      ]
    },
    {
      "type": "capability",
      "id": "create-todo"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/workspaces.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/todos.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "docs/architecture.md"
    }
  ]
}
---

# Every workspace has its own Inbox

Each workspace has exactly one Inbox project, created with it and deleted only with it. A todo created without a project lands in the person's Inbox.
