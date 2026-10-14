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
      "target": "api/services/attachments.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "web/static/js/features/todo-attachments.js"
    }
  ]
}
---

# Upload attachment

A person with access to a todo uploads files or photos to it. Uploads need a connection and count against the uploader's storage.
