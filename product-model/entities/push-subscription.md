---
{
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
      "target": "api/migrations/009_add_push_subscriptions.sql"
    }
  ]
}
---

# Push subscription

One browser or installed web app of a person that receives push notifications.

## Information kept

- **Device** — the browser endpoint notifications are delivered to
- **Subscribed at** — when it was enabled
