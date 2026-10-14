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

# Remove project member

The owner removes a member from a shared project, or withdraws a pending invitation. The membership is kept so it can be restored.
