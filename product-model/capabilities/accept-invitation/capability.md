---
{
  "availability": [
    {
      "place": "web-app::app"
    }
  ],
  "domain": "invitations",
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

# Accept invitation

A person accepts an invitation to someone else's project. The project then shows in their default workspace.
