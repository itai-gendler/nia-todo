---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "password-link",
      "effect": "creates"
    }
  ],
  "permits": [
    {
      "actors": [
        "administrator"
      ]
    },
    {
      "related": [
        {
          "verb": "has",
          "entity": "user"
        }
      ],
      "when": [
        {
          "entity": "instance-settings",
          "fact": "Email delivery",
          "is": "Configured"
        }
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/admin.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/password_setup.py"
    }
  ]
}
---

# The administrator creates password links; a person asks for a reset only while email works

A person can request a reset link for their own account only when the server can send email; the administrator can always create one.
