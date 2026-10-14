---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "user",
      "effect": "changes",
      "facts": [
        "Password",
        "Avatar",
        "Language",
        "Default reminder",
        "Dashboard sync"
      ]
    }
  ],
  "permits": [
    {
      "self": true
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
      "target": "api/routers/password_setup.py"
    }
  ]
}
---

# Only the person changes their password, avatar, language and reminder and dashboard settings

The administrator never sets a password; it is always chosen by the person, through a password link or in settings.
