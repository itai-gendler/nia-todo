---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User uploads a file of a type not allowed, over 25 MB, beyond their storage, or to a todo that already has 20 attachments",
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
          "entity": "attachment",
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
      "text": "The Product refuses and says which limit was hit",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "instance-settings",
          "effect": "reads",
          "facts": [
            "Allowed attachment types"
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

# Upload a file that is not allowed

## Trigger

A person tries to attach a video.

## Outcome

Nothing is stored.

## Edge cases

- A file whose content does not match its type is refused as not allowed.
- While the administrator has attachments disabled, uploads are refused.
