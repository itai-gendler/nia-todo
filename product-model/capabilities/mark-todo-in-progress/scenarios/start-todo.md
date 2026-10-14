---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User sets an open Todo to In progress",
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
      "text": "The Product saves the new status",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "todo",
          "effect": "changes",
          "from": "Open",
          "to": "In progress",
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

# Mark a todo in progress

## Trigger

A person starts working on a task.

## Outcome

The todo shows under In progress.
