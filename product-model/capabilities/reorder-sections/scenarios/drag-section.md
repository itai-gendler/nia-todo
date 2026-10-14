---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User drags a Section above or below another",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "section",
          "effect": "changes",
          "facts": [
            "Order"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app::project"
        }
      }
    },
    {
      "text": "The Product saves the new order of the sections",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "section",
          "effect": "changes",
          "facts": [
            "Order"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app::project"
        }
      }
    }
  ]
}
---

# Drag a section to a new position

## Trigger

A later phase becomes urgent.

## Outcome

The sections show in the new order.
