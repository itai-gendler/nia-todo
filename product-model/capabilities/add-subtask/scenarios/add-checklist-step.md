---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User types the next step on a Todo's checklist",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "todo",
          "effect": "reads",
          "facts": [
            "Title"
          ]
        },
        {
          "entity": "subtask",
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
      "text": "The Product adds the Subtask at the end of the checklist",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "subtask",
          "effect": "creates",
          "to": "Open",
          "facts": [
            "Title",
            "Order"
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

# Add a subtask

## Trigger

A person breaks a task into steps.

## Outcome

Everyone with access sees the new step and the done count.

## Edge cases

- A checklist holds up to 100 subtasks of up to 500 characters.
