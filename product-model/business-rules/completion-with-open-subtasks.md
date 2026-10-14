---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "complete-todo"
    },
    {
      "type": "entity",
      "id": "subtask"
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
      "target": "web/static/js/features/todos.js"
    }
  ]
}
---

# Completing a todo with open subtasks needs confirmation

A todo with unchecked subtasks is completed only after the person confirms; the subtasks stay as they are.
