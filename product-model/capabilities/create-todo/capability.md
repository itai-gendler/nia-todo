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
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "web/static/js/features/todo-quick-add.js"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "web/static/js/features/todo-multi-add.js"
    }
  ]
}
---

# Create todo

A person creates a todo in a project they own or are a member of, or in the Inbox when they choose none. Quick Add reads details typed into the title, several todos can be captured at once, and a todo created offline is kept on the device and created once the server is reachable.
