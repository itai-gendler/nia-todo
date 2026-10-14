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

# Set reminder

A person chooses when to be reminded about a todo. Each person keeps their own reminder on a shared todo; choosing a new time replaces their earlier one.
