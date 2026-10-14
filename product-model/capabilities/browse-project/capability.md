---
{
  "availability": [
    {
      "place": "web-app::app"
    }
  ],
  "domain": "projects",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "web/static/js/features/app-rendering.js"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "web/static/js/features/todo-rendering.js"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/todos.py"
    }
  ]
}
---

# Browse project

A person opens a project they own or are a member of and sees its todos by section, with its overview. Pinned todos come first; the person chooses whether the rest are sorted by order, priority, deadline or name.
