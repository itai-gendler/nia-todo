---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User deletes a Place",
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
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app::places-settings"
        }
      }
    },
    {
      "text": "The Product deletes it; location reminders that used it keep the address",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "place",
          "effect": "removes"
        },
        {
          "entity": "location-reminder",
          "effect": "reads",
          "facts": []
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

# Delete a place

## Trigger

A person no longer goes to the gym.

## Outcome

The place is gone from the list.
