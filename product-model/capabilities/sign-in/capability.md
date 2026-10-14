---
{
  "availability": [
    {
      "place": "web-app::sign-in"
    },
    {
      "place": "desktop-app::sign-in"
    },
    {
      "place": "android-app::sign-in"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/auth.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/services/auth.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "web/static/js/features/auth-session.js"
    }
  ]
}
---

# Sign in

A person signs in with their username, or their verified email, and password. A signed-in session lasts 30 days and is extended while it is used. Accounts that must confirm a second factor continue to that confirmation before the app opens.
