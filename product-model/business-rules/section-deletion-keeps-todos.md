---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "delete-section"
    },
    {
      "type": "entity",
      "id": "todo",
      "facts": [
        "Section"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/sections.py"
    }
  ]
}
---

# Deleting a section moves its todos to Unsorted

A section's todos stay in the project, without a section.
