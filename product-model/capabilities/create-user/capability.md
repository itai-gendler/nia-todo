---
{
  "availability": [
    {
      "place": "web-app::administration"
    }
  ],
  "domain": "users",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/admin.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "web/static/js/pages/admin.js"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/services/email_templates.py"
    }
  ]
}
---

# Create user

The administrator creates an account. Nobody signs up by themselves. The new person gets a Personal workspace with an Inbox and three starter projects, and an invitation link to choose their password: emailed when the server can send email, otherwise shown to the administrator to pass on.
