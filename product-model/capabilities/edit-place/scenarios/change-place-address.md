---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User changes the address of a Place",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "place",
          "effect": "changes",
          "facts": [
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
      "text": "The Product saves it and moves every Location reminder that uses the place to the new address",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "place",
          "effect": "changes",
          "facts": [
            "Address"
          ]
        },
        {
          "entity": "location-reminder",
          "effect": "changes",
          "facts": [
            "Address"
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

# Change a place's address

## Trigger

A person moves house.

## Outcome

Their location reminders for Home watch the new address.
