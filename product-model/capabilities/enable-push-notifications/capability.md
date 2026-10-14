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

# Enable push notifications

A person turns on push notifications for the browser or installed web app they are using, so reminders reach it.
