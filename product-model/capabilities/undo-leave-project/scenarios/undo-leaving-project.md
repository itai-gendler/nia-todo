---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User undoes leaving the project",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "project",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app"
        }
      }
    },
    {
      "text": "The Product restores their membership and the project reappears",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "project-membership",
          "effect": "changes",
          "from": "Left",
          "to": "Accepted",
          "facts": []
        },
        {
          "entity": "project",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app"
        }
      }
    }
  ]
}
---

# Undo leaving a project

## Trigger

A person left the wrong project.

## Outcome

The person is a member again.
