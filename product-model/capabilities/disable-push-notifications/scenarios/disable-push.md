---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User disables notifications for this browser",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "push-subscription",
          "effect": "reads",
          "facts": [
            "Device"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app::notification-settings"
        }
      }
    },
    {
      "text": "The Product removes the Push subscription",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "push-subscription",
          "effect": "removes"
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

# Disable push notifications for this browser

## Trigger

A person gets reminders on their phone and not on the office computer.

## Outcome

This browser no longer receives push notifications; the person's other subscriptions stay.
