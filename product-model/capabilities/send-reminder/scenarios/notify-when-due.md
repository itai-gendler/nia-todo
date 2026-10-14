---
{
  "kind": "primary",
  "routes": {
    "web": "Web",
    "desktop": "Desktop app",
    "android": "Android app"
  },
  "steps": [
    {
      "text": "The time of a scheduled Reminder is reached while its todo is open or in progress",
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
          "entity": "todo",
          "effect": "reads",
          "facts": [
            "Title"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app"
        },
        "desktop": {
          "place": "desktop-app::app"
        },
        "android": {
          "place": "android-app::app"
        }
      }
    },
    {
      "text": "The Product notifies the person with the todo's title on their devices and marks the Reminder sent",
      "kind": "product",
      "entities": [
        {
          "entity": "reminder",
          "effect": "changes",
          "from": "Scheduled",
          "to": "Sent",
          "facts": []
        },
        {
          "entity": "todo",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app"
        },
        "desktop": {
          "place": "desktop-app::app"
        },
        "android": {
          "place": "android-app::app"
        }
      }
    }
  ]
}
---

# Notify a person when their reminder is due

## Trigger

The reminder time arrives.

## Outcome

The person is notified once.

## Edge cases

- A reminder on a done todo is not sent.
