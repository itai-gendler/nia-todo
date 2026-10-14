---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "project",
      "facts": [
        "Parent project",
        "Workspace"
      ]
    },
    {
      "type": "capability",
      "id": "create-project"
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

# A subproject is in the same workspace as its parent and never under itself

A parent is one of the owner's own projects in the same workspace, and a project can never become its own ancestor.
