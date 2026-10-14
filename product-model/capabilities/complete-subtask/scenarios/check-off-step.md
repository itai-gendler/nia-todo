---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User checks off a Subtask",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "subtask",
          "effect": "reads",
          "facts": [
            "Title"
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
      "text": "The Product marks it done and updates the done count",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "subtask",
          "effect": "changes",
          "from": "Open",
          "to": "Done",
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

# Check off a subtask

## Trigger

A person finished one step.

## Outcome

The todo shows how many of its subtasks are done.
