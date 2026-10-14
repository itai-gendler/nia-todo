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
    }
  ]
}
---

# Send password link

The administrator gives a person a link to choose a new password; administrators never set passwords themselves. A new link replaces the person's earlier active one.
