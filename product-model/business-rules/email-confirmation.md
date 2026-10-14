---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "change-profile-settings"
    },
    {
      "type": "capability",
      "id": "confirm-email"
    },
    {
      "type": "entity",
      "id": "user",
      "facts": [
        "Pending email",
        "Email verified"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/services/email_verification.py"
    }
  ]
}
---

# A new email address needs confirmation when the server can send email

With email delivery configured a new address stays pending until confirmed through the emailed link, and the old one stays in use. Without it, a person's own change is saved unverified and an administrator's change is saved as verified.
