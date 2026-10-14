---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "delete-done-todos"
    },
    {
      "type": "entity",
      "id": "todo",
      "effect": "removes",
      "from": "Done"
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

# Deleting a project's done todos includes its subprojects

Clearing done todos removes the completed todos of the project and of every project under it.
