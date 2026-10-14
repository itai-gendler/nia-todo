---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User accepts an invitation to a Project",
      "kind": "actor",
      "actor": "user",
      "entities": [
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
          "facts": [
            "Name",
            "Color"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app::invitations"
        }
      }
    },
    {
      "text": "The Product makes them a member and shows the project in their default workspace",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "project-membership",
          "effect": "changes",
          "from": "Pending",
          "to": "Accepted",
          "facts": [
            "Display workspace"
          ]
        },
        {
          "entity": "workspace",
          "effect": "reads",
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
          "place": "web-app::app::invitations"
        }
      }
    }
  ]
}
---

# Accept an invitation

## Trigger

A person receives an invitation.

## Outcome

The person works in the shared project; its owner is told.
