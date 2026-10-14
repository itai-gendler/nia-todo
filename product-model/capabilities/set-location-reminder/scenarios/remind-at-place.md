---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User turns on Remind me when arriving at or leaving a place, picks the trigger and a saved place or an address",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "place",
          "effect": "reads",
          "facts": [
            "Name",
            "Address"
          ]
        },
        {
          "entity": "location-reminder",
          "effect": "creates",
          "facts": [
            "Trigger",
            "Address"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app::todo-editor"
        }
      }
    },
    {
      "text": "The Product saves the Location reminder for the person, taking the address from the place when one was chosen",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "location-reminder",
          "effect": "creates",
          "facts": [
            "Trigger",
            "Address",
            "Enabled"
          ]
        },
        {
          "entity": "place",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app::todo-editor"
        }
      }
    }
  ]
}
---

# Set a location reminder

## Trigger

A person wants to remember the parcel when they get home.

## Outcome

The person's Android app will remind them at the place.

## Edge cases

- Without a place or an address the location reminder is refused.
