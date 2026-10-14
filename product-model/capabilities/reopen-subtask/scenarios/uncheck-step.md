---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User unchecks a done Subtask",
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
      "text": "The Product opens it again",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "subtask",
          "effect": "changes",
          "from": "Done",
          "to": "Open",
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

# Uncheck a subtask

## Trigger

A step needs redoing.

## Outcome

The subtask is open again.
