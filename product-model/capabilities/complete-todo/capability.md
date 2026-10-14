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

# Complete todo

A person marks a todo done. A todo with open subtasks needs confirmation, and completing a repeating todo creates its next occurrence.
