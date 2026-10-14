---
{
  "availability": [
    {
      "place": "web-app::app"
    }
  ],
  "domain": "api-keys",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/auth.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "web/static/js/features/api-keys.js"
    }
  ]
}
---

# Create API key

A person creates a named API key for an automation. The full key is shown once. On an account with two-factor authentication this needs a fresh second-factor confirmation.
