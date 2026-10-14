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
      "target": "api/routers/projects.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "web/static/js/features/projects.js"
    }
  ]
}
---

# Delete done todos

A person clears a project's completed todos, including those in the project's subprojects, permanently.
