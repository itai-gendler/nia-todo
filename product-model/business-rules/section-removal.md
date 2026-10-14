---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "section",
      "effect": "removes"
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "has",
          "entity": "project"
        },
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
          "entity": "project"
        },
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
      "target": "api/routers/sections.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/services/sharing.py"
    }
  ]
}
---

# The owner and members of a project deletes its sections

Anyone who works in a project deletes its sections, not only its owner.
