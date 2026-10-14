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

# Create project

A person creates a project in one of their workspaces, optionally as a subproject of another of their projects there.
