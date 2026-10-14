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
      "target": "api/routers/setup.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/services/setup_token.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "web/static/js/pages/setup.js"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "README.md"
    }
  ]
}
---

# Complete first-run setup

The person installing a new server proves they run it with the one-time setup token from the server log, sets the admin password and creates the first account. Setup runs once; the token is deleted afterwards.
