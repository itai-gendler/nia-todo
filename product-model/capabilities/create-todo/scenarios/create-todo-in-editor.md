---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User enters a title and, if needed, a description, priority, project, section and deadline",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "todo",
          "effect": "creates",
          "facts": [
            "Title",
            "Description",
            "Priority",
            "Project",
            "Section",
            "Deadline"
          ],
          "to": "Open"
        },
        {
          "entity": "project",
          "effect": "reads",
          "facts": []
        },
        {
          "entity": "section",
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
      "text": "The Product creates the open Todo in the chosen project, or in the Inbox when none is chosen",
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
          "entity": "project",
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

# Create a todo

## Trigger

Something comes to mind that needs doing.

## Outcome

The todo is in its project for the person and every member of it.
