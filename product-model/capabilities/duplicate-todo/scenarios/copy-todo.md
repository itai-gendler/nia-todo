---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User duplicates a Todo",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "todo",
          "as": "original-todo",
          "effect": "reads",
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
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app"
        }
      }
    },
    {
      "text": "The Product creates an open copy in the same project with unchecked subtasks and the same reminders, and offers to undo",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "todo",
          "as": "copy",
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
          "entity": "subtask",
          "effect": "creates",
          "to": "Open",
          "facts": [
            "Title",
            "Order"
          ],
          "with": "copy"
        },
        {
          "entity": "reminder",
          "effect": "creates",
          "to": "Scheduled",
          "facts": [
            "Remind at",
            "Source"
          ],
          "with": "copy"
        },
        {
          "entity": "location-reminder",
          "effect": "creates",
          "facts": [
            "Trigger",
            "Address",
            "Enabled"
          ],
          "with": "copy"
        },
        {
          "entity": "project",
          "effect": "reads",
          "facts": []
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

# Duplicate a todo

## Trigger

A person needs the same checklist for a second trip.

## Outcome

An independent copy of the todo exists.
