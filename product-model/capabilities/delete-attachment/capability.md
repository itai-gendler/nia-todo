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
      "target": "web/static/js/features/todo-attachments.js"
    }
  ]
}
---

# Delete attachment

A person with access to a todo deletes one of its attachments after confirming, freeing the uploader's storage.
