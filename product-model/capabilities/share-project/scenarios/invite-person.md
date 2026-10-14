---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User enters the username or email of the person to invite to a Project they own",
      "kind": "actor",
      "actor": "user",
      "entities": [
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
          "place": "web-app::app::project-editor"
        }
      }
    },
    {
      "text": "A person with that username, or with that verified email, exists and has no access or pending invitation yet",
      "kind": "condition",
      "actor": "user",
      "entities": [
        {
          "entity": "user",
          "as": "invitee",
          "effect": "reads",
          "facts": [
            "Username",
            "Email",
            "Email verified"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app::project-editor"
        }
      }
    },
    {
      "text": "The Product creates a pending invitation and emails the invitee when it can",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "project-membership",
          "effect": "creates",
          "to": "Pending",
          "facts": [
            "Invited by",
            "Invited with"
          ]
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

# Invite a person to a project

## Trigger

A person wants their partner to work on the shopping list with them.

## Outcome

The invitee sees the invitation; the owner sees them as pending in the member list.

## Edge cases

- An email address only finds a person whose email is verified; a username always does.
