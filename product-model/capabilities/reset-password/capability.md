---
{
  "availability": [
    {
      "place": "web-app::sign-in"
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
      "target": "web/static/js/pages/set-password.js"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "web/static/js/features/auth-session.js"
    }
  ]
}
---

# Reset password

A person who forgot their password asks for a reset link by username or email and chooses a new password through it. It exists only while the server can send email, and only accounts with a verified email receive the link.
