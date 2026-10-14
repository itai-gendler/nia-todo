---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User declines an invitation to a Project",
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
            "Name"
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
      "text": "The Product records the decline and tells the owner",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "project-membership",
          "effect": "changes",
          "from": "Pending",
          "to": "Declined",
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

# Decline an invitation

## Trigger

A person does not want to join.

## Outcome

The invitation is gone; the owner may invite them again later.
