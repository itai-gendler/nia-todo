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
      "target": "web/static/js/features/todos.js"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/migrations/037_add_todo_pins.sql"
    }
  ]
}
---

# Pin todo

A person pins a todo so it stays at the top of its lists.
