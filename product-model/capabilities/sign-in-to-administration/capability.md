---
{
  "availability": [
    {
      "place": "web-app::sign-in"
    },
    {
      "place": "web-app::administration"
    }
  ],
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

# Sign in to administration

The administrator opens the administration area with the admin password. The administration session lasts one day.
