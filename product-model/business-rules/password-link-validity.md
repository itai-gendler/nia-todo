---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "password-link",
      "facts": [
        "Expires at"
      ]
    },
    {
      "type": "entity",
      "id": "instance-settings",
      "facts": [
        "Password link validity"
      ]
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
      "target": "api/services/email_config.py"
    }
  ]
}
---

# Password links work once and expire

A password link works once, within the password link validity (24 hours unless the administrator sets 1 to 168), and a new link of the same purpose replaces the earlier one.
