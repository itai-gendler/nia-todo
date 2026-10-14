---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User removes a member from a Project they own and confirms",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "user",
          "as": "member",
          "effect": "reads",
          "facts": [
            "Display name",
            "Username"
          ]
        },
        {
          "entity": "project-membership",
          "effect": "reads",
          "facts": [
            "Invited by"
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
          "place": "web-app::app::project-editor"
        }
      }
    },
    {
      "text": "The Product removes their access; the project disappears for them",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "project-membership",
          "effect": "changes",
          "from": "Accepted",
          "to": "Removed",
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
          "place": "web-app::app::project-editor"
        }
      }
    }
  ]
}
---

# Remove a member

## Trigger

A colleague moved to another team.

## Outcome

The removed person no longer sees the project; the owner can undo it right away.
