---
{
  "availability": [
    {
      "place": "web-app::administration"
    }
  ],
  "domain": "email",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/admin.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/services/email.py"
    }
  ]
}
---

# Send test email

The administrator sends a test email to check the mail settings.
