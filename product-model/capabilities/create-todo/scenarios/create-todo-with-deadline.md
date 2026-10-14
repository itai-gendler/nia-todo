---
{
  "kind": "alternative",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User creates a todo with a deadline and no reminder time",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "todo",
          "effect": "creates",
          "facts": [
            "Title",
            "Deadline"
          ],
          "to": "Open"
        },
        {
          "entity": "reminder",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app::todo-editor"
        }
      }
    },
    {
      "text": "The person has a default reminder set",
      "kind": "condition",
      "actor": "user",
      "entities": [
        {
          "entity": "user",
          "effect": "reads",
          "facts": [
            "Default reminder"
          ]
        },
        {
          "entity": "reminder",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app::todo-editor"
        }
      }
    },
    {
      "text": "The Product creates the Todo and an automatic Reminder that long before the deadline",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "todo",
          "effect": "creates",
          "to": "Open",
          "facts": [
            "Title",
            "Description",
            "Priority",
            "Pinned",
            "Project",
            "Section",
            "Deadline",
            "Repeat"
          ]
        },
        {
          "entity": "reminder",
          "effect": "creates",
          "to": "Scheduled",
          "facts": [
            "Remind at",
            "Source"
          ],
          "with": "todo"
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

# Create a todo with a deadline and an automatic reminder

## Trigger

A person adds a todo due tomorrow at noon.

## Outcome

The person will be reminded ahead of the deadline without setting a time.
