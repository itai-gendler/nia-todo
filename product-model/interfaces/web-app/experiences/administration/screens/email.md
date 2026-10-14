---
{
  "entities": [
    {
      "entity": "instance-settings",
      "shows": [
        "Email delivery"
      ],
      "collects": [
        "Email delivery",
        "Password link validity"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "web/admin.html"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "web/static/js/pages/admin.js"
    }
  ]
}
---

# Email / SMTP

How the server sends email, and a test send.
