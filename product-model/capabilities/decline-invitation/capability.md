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

# Decline invitation

A person declines an invitation to someone else's project.
