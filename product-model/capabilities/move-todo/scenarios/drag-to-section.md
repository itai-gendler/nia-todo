---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User drags a Todo into another Section of the project",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "todo",
          "effect": "changes",
          "facts": [
            "Section"
          ]
        },
        {
          "entity": "project",
          "effect": "reads",
          "facts": []
        },
        {
          "entity": "section",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app::project"
        }
      }
    },
    {
      "text": "The Product saves the new section",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "todo",
          "effect": "changes",
          "facts": [
            "Section"
          ]
        },
        {
          "entity": "section",
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

# Drag a todo to another section

## Trigger

A task moves to the next phase.

## Outcome

The todo shows in its new section for everyone in the project.
