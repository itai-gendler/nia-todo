---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User deletes a Subtask and confirms",
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
      "text": "The Product removes it from the checklist",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "subtask",
          "effect": "removes",
          "from": "Open"
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

# Delete a subtask

## Trigger

A step is no longer needed.

## Outcome

The checklist no longer has the step.
