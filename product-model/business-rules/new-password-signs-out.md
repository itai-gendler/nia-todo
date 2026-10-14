---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "user",
      "facts": [
        "Password"
      ]
    },
    {
      "type": "capability",
      "id": "change-password"
    },
    {
      "type": "capability",
      "id": "reset-password"
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

# A new password signs the account out everywhere

Changing or resetting a password ends every session of the account.
