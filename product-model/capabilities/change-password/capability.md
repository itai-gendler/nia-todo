---
{
  "availability": [
    {
      "place": "web-app::app"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/me.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "web/static/js/features/security-dialogs.js"
    }
  ]
}
---

# Change password

A signed-in person changes their password by giving the current one. On an account with two-factor authentication the change needs a fresh second-factor confirmation. Changing it signs the account out everywhere.
