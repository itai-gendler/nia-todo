---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User undoes the removal they just made",
      "kind": "actor",
      "actor": "user",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web-app::app"
        }
      }
    },
    {
      "text": "The Product restores the membership and shows the project in the member's default workspace again",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "project-membership",
          "effect": "changes",
          "from": "Removed",
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
          "place": "web-app::app"
        }
      }
    }
  ]
}
---

# Undo removing a member

## Trigger

An owner removed the wrong member.

## Outcome

The member is back in the project.
