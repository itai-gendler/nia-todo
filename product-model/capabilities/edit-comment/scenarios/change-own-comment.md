---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User changes the text of a Comment they wrote",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "comment",
          "effect": "changes",
          "facts": [
            "Body"
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
      "text": "The Product saves it and records when it was edited",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "comment",
          "effect": "changes",
          "facts": [
            "Body",
            "Edited at"
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

# Edit one's own comment

## Trigger

A person fixes a typo in their comment.

## Outcome

The comment shows its new text.
