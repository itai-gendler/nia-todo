---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User clears the reminder of a Todo",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "reminder",
          "effect": "reads",
          "facts": [
            "Remind at"
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
    },
    {
      "text": "The Product removes the person's Reminder",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "reminder",
          "effect": "removes",
          "from": "Scheduled"
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

# Remove a reminder

## Trigger

A person no longer needs the nudge.

## Outcome

The person is not reminded; other members' reminders stay.
