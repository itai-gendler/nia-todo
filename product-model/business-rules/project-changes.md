---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "project",
      "effect": "changes"
    }
  ],
  "permits": [
    {
      "related": [
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
      "target": "api/routers/projects.py"
    }
  ]
}
---

# Only the owner edits a project

Members of a shared project cannot rename, recolor, re-parent or move it; they only choose where it shows for them.
