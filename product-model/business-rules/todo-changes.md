---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "todo",
      "effect": "changes"
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "contains",
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
          "verb": "contains",
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
    },
    {
      "related": [
        {
          "verb": "creates",
          "entity": "user"
        }
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/todos.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/services/sharing.py"
    }
  ]
}
---

# The owner, the members and the creator of a todo change it

Members change todos in a shared project exactly as the owner does, including other people's todos.
