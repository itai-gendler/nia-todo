---
{
  "availability": [
    {
      "place": "web-app::app"
    }
  ],
  "domain": "profile",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/me.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/services/email_verification.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "web/static/js/features/user-settings.js"
    }
  ]
}
---

# Change profile settings

A person changes their avatar, display name and email address in Profile. A new email address needs confirmation when the server can send email; changing it on an account with two-factor authentication needs a fresh second-factor confirmation.
