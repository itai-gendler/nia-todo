---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User picks +1 hour, This evening, Tomorrow morning, Weekend or Next week for a Todo",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "todo",
          "effect": "reads",
          "facts": [
            "Title",
            "Deadline"
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
      "text": "The Product moves the deadline there, shifts the Reminder by the same amount, and offers to undo",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "todo",
          "effect": "changes",
          "facts": [
            "Deadline"
          ]
        },
        {
          "entity": "reminder",
          "effect": "changes",
          "facts": [
            "Remind at",
            "Source"
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

# Move a todo to later

## Trigger

A person cannot get to a task today.

## Outcome

The todo is due later and reminds the person at the matching later time.
