---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User sends a test",
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
      "text": "The Product sends a test notification to every Push subscription of the person and says whether it was delivered",
      "kind": "product",
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
    }
  ]
}
---

# Send a test notification

## Trigger

A person wonders why reminders do not arrive.

## Outcome

The person sees the test arrive, or is told no subscription accepted it.
