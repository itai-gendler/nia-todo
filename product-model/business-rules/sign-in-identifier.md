---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "sign-in"
    },
    {
      "type": "capability",
      "id": "share-project"
    },
    {
      "type": "entity",
      "id": "user",
      "facts": [
        "Username",
        "Email",
        "Email verified"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/services/auth.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/sharing.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/password_setup.py"
    }
  ]
}
---

# People sign in with their username or a verified email

An email address signs a person in, and finds them for an invitation or a password reset, only once it is verified.
