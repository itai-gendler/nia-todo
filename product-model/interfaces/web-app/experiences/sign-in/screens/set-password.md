---
{
  "entities": [
    {
      "entity": "password-link",
      "shows": [
        "Purpose",
        "Expires at"
      ]
    },
    {
      "entity": "user",
      "shows": [
        "Username",
        "Display name"
      ],
      "collects": [
        "Password"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "web/set-password.html"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "web/static/js/pages/set-password.js"
    }
  ]
}
---

# Set password

Where a person opens a password link, sees whose account it is for, and chooses a password.
