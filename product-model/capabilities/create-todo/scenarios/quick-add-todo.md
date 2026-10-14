---
{
  "kind": "alternative",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User types a title with details, such as \"Milk tomorrow 18:00 remind:17:30 repeat:weekly #Shopping /Cold !high\"",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "todo",
          "effect": "creates",
          "facts": [
            "Title"
          ],
          "to": "Open"
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app::todo-editor"
        }
      }
    },
    {
      "text": "The Product recognizes the deadline, reminder, repeat, location, project, section and priority and shows what it detected",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "project",
          "effect": "reads",
          "facts": [
            "Name"
          ]
        },
        {
          "entity": "section",
          "effect": "reads",
          "facts": [
            "Name"
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
      "text": "The Product creates the Todo with those details and a Reminder at the chosen time",
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

# Create a todo with Quick Add

## Trigger

A person captures a todo in one line.

## Outcome

The todo has its details without opening each field.

## Edge cases

- Quick Add words follow the app language.
