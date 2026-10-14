---
{
  "entities": [
    {
      "entity": "user",
      "shows": [
        "Username",
        "First user",
        "Email",
        "Email verified"
      ],
      "collects": [
        "Username",
        "Display name",
        "Email",
        "Language",
        "BrainDump access",
        "Attachment quota"
      ]
    },
    {
      "entity": "password-link",
      "shows": [
        "Purpose"
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

# Users

Every account with its email state, storage use and access, and the controls to create, edit and delete accounts and send password links.
