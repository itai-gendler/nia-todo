---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User sets a repeat but no deadline",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "todo",
          "effect": "creates",
          "facts": [
            "Repeat"
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
      "text": "The Product refuses: a repeating todo needs a deadline to start from",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "todo",
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

# Create a repeating todo without a deadline

## Trigger

A person wants a weekly todo but forgets the date.

## Outcome

No todo is created until a deadline is set.
