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

# Edit todo

A person with access to a todo changes its title, description, priority, project, section, deadline, repeat or pin in the todo editor. Status changes have their own controls.
