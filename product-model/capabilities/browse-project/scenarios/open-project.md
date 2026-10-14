---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User opens a Project",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "project",
          "effect": "reads",
          "facts": [
            "Name",
            "Color",
            "Icon"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app::project"
        }
      }
    },
    {
      "text": "The Product shows the project's sections in order with their todos, todos without a section under Unsorted, pinned todos first",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "section",
          "effect": "reads",
          "facts": [
            "Name",
            "Order"
          ]
        },
        {
          "entity": "todo",
          "effect": "reads",
          "facts": [
            "Title",
            "Priority",
            "Pinned",
            "Section",
            "Deadline",
            "Repeat"
          ]
        },
        {
          "entity": "project",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app::project"
        }
      }
    }
  ]
}
---

# Open a project

## Trigger

A person wants to see what is left in a project.

## Outcome

The person sees the project's open todos; done todos appear only when they choose to show them.

## Edge cases

- A shared project also shows who shared it.
