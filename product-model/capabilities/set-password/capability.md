---
{
  "availability": [
    {
      "place": "web-app::sign-in"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/password_setup.py"
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

A person opens the invitation link the administrator sent and chooses the password for their new account. Setting it also confirms their email address.
