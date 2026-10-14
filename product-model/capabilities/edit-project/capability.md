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

# Edit project

The owner changes a project's name, color, icon, parent or workspace. Moving a project to another workspace moves its subprojects with it; the Inbox stays in its workspace.
