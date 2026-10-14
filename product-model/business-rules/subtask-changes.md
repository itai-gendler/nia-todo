---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "subtask",
      "effect": "changes"
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
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/services/sharing.py"
    }
  ]
}
---

# Whoever can see a todo changes its subtasks

A todo's checklist is shared by everyone with access to the todo.
