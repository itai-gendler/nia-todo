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

# Revoke API key

A person revokes one of their API keys. On an account with two-factor authentication this needs a fresh second-factor confirmation.
