---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User enables notifications and allows them in the browser",
      "kind": "actor",
      "actor": "user",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web-app::app::notification-settings"
        }
      }
    },
    {
      "text": "The Product registers this browser as a Push subscription",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "push-subscription",
          "effect": "creates",
          "facts": [
            "Device",
            "Subscribed at"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app::notification-settings"
        }
      }
    }
  ]
}
---

# Enable push notifications for this browser

## Trigger

A person wants reminders even when the app is closed.

## Outcome

Reminders and tests reach this browser.
