---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User changes the text of a Subtask",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "subtask",
          "effect": "changes",
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
      "text": "The Product saves it",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "subtask",
          "effect": "changes",
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
    }
  ]
}
---

# Edit a subtask

## Trigger

A step needs a clearer wording.

## Outcome

The subtask shows its new text.
