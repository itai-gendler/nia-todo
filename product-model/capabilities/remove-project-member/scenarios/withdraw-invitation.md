---
{
  "kind": "alternative",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User removes a pending invitee from a Project they own",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "project-membership",
          "effect": "reads",
          "facts": [
            "Invited by",
            "Invited with"
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
      "text": "The Product withdraws the invitation; it disappears for the invitee",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "project-membership",
          "effect": "changes",
          "from": "Pending",
          "to": "Removed",
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

# Withdraw a pending invitation

## Trigger

An owner invited the wrong person.

## Outcome

The invitation is gone.
