---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User deletes a Todo and confirms",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "todo",
          "effect": "reads",
          "facts": [
            "Title"
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
      "text": "The Product removes it at once on the device and offers to undo",
      "kind": "product",
      "actor": "user",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web-app::app"
        }
      }
    },
    {
      "text": "The Product deletes the todo with its subtasks, comments, attachments and reminders once the undo time has passed",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "todo",
          "effect": "removes",
          "from": "Open"
        },
        {
          "entity": "subtask",
          "effect": "removes",
          "from": "Open",
          "with": "todo"
        },
        {
          "entity": "comment",
          "effect": "removes",
          "with": "todo"
        },
        {
          "entity": "attachment",
          "effect": "removes",
          "with": "todo"
        },
        {
          "entity": "reminder",
          "effect": "removes",
          "from": "Scheduled",
          "with": "todo"
        },
        {
          "entity": "location-reminder",
          "effect": "removes",
          "with": "todo"
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

# Delete a todo

## Trigger

A todo was created by mistake.

## Outcome

The todo is gone for everyone in the project.

## Edge cases

- Undoing within a few seconds keeps the todo as it was.
