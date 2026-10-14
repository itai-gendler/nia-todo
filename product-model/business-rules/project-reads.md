---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "project",
      "effect": "reads"
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
    },
    {
      "related": [
        {
          "verb": "has",
          "entity": "project-membership"
        },
        {
          "verb": "holds",
          "entity": "user"
        }
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/services/sharing.py"
    }
  ]
}
---

# Only the owner and accepted members see a project

A project is visible to its owner and to the people who accepted an invitation to it.
