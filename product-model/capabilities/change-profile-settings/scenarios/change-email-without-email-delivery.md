---
{
  "kind": "alternative",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User enters a new email address",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "user",
          "effect": "changes",
          "facts": [
            "Email"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app::profile-settings"
        }
      }
    },
    {
      "text": "The server has no email delivery configured",
      "kind": "condition",
      "actor": "user",
      "entities": [
        {
          "entity": "instance-settings",
          "effect": "reads",
          "facts": [
            "Email delivery"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app::profile-settings"
        }
      }
    },
    {
      "text": "The Product saves the new address as unverified",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "user",
          "effect": "changes",
          "facts": [
            "Email",
            "Email verified"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app::profile-settings"
        }
      }
    }
  ]
}
---

# Change the email address on a server that cannot send email

## Trigger

A person changes their address on a server without email.

## Outcome

The new address is stored but cannot be used to sign in or to be invited until it is verified.
