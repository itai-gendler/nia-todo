---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User picks a reminder date and time for a Todo",
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
        },
        {
          "entity": "reminder",
          "as": "new-reminder",
          "effect": "creates",
          "facts": [
            "Remind at"
          ],
          "to": "Scheduled"
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app::todo-editor"
        }
      }
    },
    {
      "text": "The Product replaces the person's earlier Reminder on the todo with one at the chosen time",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "reminder",
          "as": "earlier-reminder",
          "effect": "removes",
          "from": "Scheduled"
        },
        {
          "entity": "reminder",
          "as": "new-reminder",
          "effect": "creates",
          "to": "Scheduled",
          "facts": [
            "Remind at",
            "Source"
          ]
        },
        {
          "entity": "todo",
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

# Set a reminder on a todo

## Trigger

A person wants a nudge the evening before.

## Outcome

The person, and only the person, will be reminded at that time.
