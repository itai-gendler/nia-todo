---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "delete-project"
    },
    {
      "type": "entity",
      "id": "todo",
      "facts": [
        "Project",
        "Section"
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

# Deleting a project moves its todos to their creators' inboxes

When a project is deleted, its subprojects and sections go with it, and every todo in them moves to the Inbox of the person who created it, without a section.
