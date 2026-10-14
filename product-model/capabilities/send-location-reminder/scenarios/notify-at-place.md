---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The phone arrives at, or leaves, the address of an enabled Location reminder with that trigger",
      "kind": "condition",
      "unattended": true,
      "entities": [
        {
          "entity": "location-reminder",
          "effect": "reads",
          "facts": [
            "Trigger",
            "Address",
            "Enabled"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "android-app::app"
        }
      }
    },
    {
      "text": "The Product shows a notification with the todo's title",
      "kind": "product",
      "entities": [
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
          "place": "android-app::app"
        }
      }
    }
  ]
}
---

# Notify a person at a place

## Trigger

A person comes home.

## Outcome

The person is reminded of the todo at the place.

## Edge cases

- No notification appears while the app lacks location or notification permission.
