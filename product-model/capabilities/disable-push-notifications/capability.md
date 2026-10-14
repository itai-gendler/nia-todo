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
      "target": "web/static/js/features/push-notifications.js"
    }
  ]
}
---

# Disable push notifications

A person turns off push notifications for the browser they are using.
