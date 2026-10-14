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
      "target": "api/services/email_config.py"
    }
  ]
}
---

# Change email settings

The administrator configures the outgoing mail server and how long password and confirmation links stay valid. With email configured, invitations, password resets, email confirmations and project invitations go out by email.
