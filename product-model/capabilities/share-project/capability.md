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
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/services/email_templates.py"
    }
  ]
}
---

# Share project

The owner invites another person on the server to a project by username or verified email. The invitee is emailed when the server can send email and their address is verified, and always sees the invitation in the app.
