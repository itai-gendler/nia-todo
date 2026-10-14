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

# Edit user

The administrator changes an account's username, display name or email, its BrainDump access, or its attachment storage quota. A new email needs confirmation by the person when the server can send email; otherwise the administrator's address counts as verified.
