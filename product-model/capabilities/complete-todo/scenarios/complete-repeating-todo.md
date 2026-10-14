---
{
  "kind": "alternative",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User checks off a repeating Todo",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "todo",
          "as": "completed-todo",
          "effect": "reads",
          "facts": [
            "Title",
            "Repeat",
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
      "text": "The Product marks it done and creates the next occurrence: the deadline advanced by the repeat, subtasks unchecked, and the reminder moved along",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "todo",
          "as": "completed-todo",
          "effect": "changes",
          "from": "Open",
          "to": "Done",
          "facts": [
            "Completed at"
          ]
        },
        {
          "entity": "todo",
          "as": "next-occurrence",
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
            "Repeat",
            "Series"
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
          "with": "next-occurrence"
        },
        {
          "entity": "reminder",
          "effect": "creates",
          "to": "Scheduled",
          "facts": [
            "Remind at",
            "Source"
          ],
          "with": "next-occurrence"
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

# Complete a repeating todo

## Trigger

A person takes out the bins, a weekly todo.

## Outcome

Next week's occurrence is waiting with the same details.

## Edge cases

- A monthly todo due on the 31st falls on the last day of shorter months.
- The next deadline keeps the same local time across daylight-saving changes.
- Completing the same occurrence twice does not create a second next occurrence.
