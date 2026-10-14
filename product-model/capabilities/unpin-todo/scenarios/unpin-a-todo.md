---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User unpins a pinned Todo",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "todo",
          "effect": "reads",
          "facts": [
            "Title",
            "Pinned"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app"
        }
      }
    },
    {
      "text": "The Product removes the pin",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "todo",
          "effect": "changes",
          "facts": [
            "Pinned"
          ]
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

# Unpin a todo

## Trigger

A pinned todo is no longer pressing.

## Outcome

The todo returns to its normal place.
