---
{
  "kind": "edge",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The time of a scheduled Reminder is reached and the person has no push subscription or connected desktop app",
      "kind": "condition",
      "unattended": true,
      "entities": [
        {
          "entity": "reminder",
          "effect": "reads",
          "facts": [
            "Remind at"
          ]
        },
        {
          "entity": "push-subscription",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app"
        }
      }
    },
    {
      "text": "The Product keeps the Reminder scheduled and tries again every 30 seconds",
      "kind": "product",
      "entities": [
        {
          "entity": "reminder",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app"
        }
      }
    }
  ]
}
---

# Hold a reminder while no device can receive it

## Trigger

A person has push turned off and the desktop app closed.

## Outcome

The reminder goes out as soon as a device can receive it.
