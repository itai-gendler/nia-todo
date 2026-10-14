---
{
  "kind": "edge",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User accepts an invitation the owner has just withdrawn",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "project-membership",
          "effect": "reads",
          "facts": [
            "Invited by"
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
      "text": "The Product refuses because the invitation is no longer pending",
      "kind": "product",
      "actor": "user",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web-app::app::invitations"
        }
      }
    }
  ]
}
---

# Answer an invitation that is no longer pending

## Trigger

The owner withdrew the invitation while the invitee was answering.

## Outcome

Nothing changes; the invitation disappears.
