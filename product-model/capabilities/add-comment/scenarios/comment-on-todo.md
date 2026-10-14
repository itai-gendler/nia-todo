---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User writes a Comment on a Todo",
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
          "entity": "comment",
          "effect": "creates",
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
      "text": "The Product adds it with the author and time",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "comment",
          "effect": "creates",
          "facts": [
            "Body",
            "Written at"
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

# Comment on a todo

## Trigger

A member has a question about a shared todo.

## Outcome

Everyone in the project sees the comment at once.

## Edge cases

- An empty comment, or one over 5,000 characters, is refused.
