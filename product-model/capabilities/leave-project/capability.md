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
      "target": "api/routers/sharing.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "web/static/js/features/project-sharing.js"
    }
  ]
}
---

# Leave project

A member leaves a project shared with them. The owner cannot leave their own project.
