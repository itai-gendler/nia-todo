---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "attachment",
      "effect": "reads"
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "has",
          "entity": "todo"
        },
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
          "verb": "has",
          "entity": "todo"
        },
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
          "verb": "has",
          "entity": "todo"
        },
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
    }
  ]
}
---

# Whoever can see a todo opens its attachments

Attachments are as visible as their todo.
