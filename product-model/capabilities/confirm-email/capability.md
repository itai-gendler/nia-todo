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
    }
  ]
}
---

# Confirm email

A person confirms a new email address by opening the link emailed to it while signed in. Until then the old address stays in use.
