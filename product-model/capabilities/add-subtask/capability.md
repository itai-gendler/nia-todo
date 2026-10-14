---
{
  "availability": [
    {
      "place": "web-app::app"
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

# Add subtask

A person adds a step to a todo's checklist. Subtasks need a connection, and a new todo must be saved first.
