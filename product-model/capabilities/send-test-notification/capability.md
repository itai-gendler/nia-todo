---
{
  "availability": [
    {
      "place": "web-app::app"
    }
  ],
  "domain": "notifications",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/push.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/services/push.py"
    }
  ]
}
---

# Send test notification

A person sends a test notification to check push works.
