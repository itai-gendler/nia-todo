---
{
  "kind": "alternative",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User changes the deadline of a Todo whose Reminder follows the deadline automatically",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "reminder",
          "effect": "reads",
          "facts": [
            "Remind at",
            "Source"
          ]
        },
        {
          "entity": "todo",
          "effect": "changes",
          "facts": [
            "Deadline"
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
      "text": "The Product saves the deadline and moves the person's automatic reminder with it",
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
            "Remind at"
          ]
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

# Move a deadline with an automatic reminder

## Trigger

A due date slips by a day.

## Outcome

The reminder still fires the same time before the new deadline; a reminder the person chose stays where it is.
