---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User enters a label and an address",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "place",
          "effect": "creates",
          "facts": [
            "Name",
            "Address"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app::places-settings"
        }
      }
    },
    {
      "text": "The Product saves the Place",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "place",
          "effect": "creates",
          "facts": [
            "Name",
            "Address",
            "Icon"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app::places-settings"
        }
      }
    }
  ]
}
---

# Save a place

## Trigger

A person wants reminders when they get home.

## Outcome

The place can be chosen for location reminders.

## Edge cases

- A label and an address are both required; a label the person already uses is refused.
