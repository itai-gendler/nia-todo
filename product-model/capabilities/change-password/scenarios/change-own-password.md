---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User enters their current password and a new one",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "user",
          "effect": "changes",
          "facts": [
            "Password"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app::security-settings"
        }
      }
    },
    {
      "text": "The Product saves the new password and signs the account out of every device",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "user",
          "effect": "changes",
          "facts": [
            "Password"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app::security-settings"
        }
      }
    }
  ]
}
---

# Change the password

## Trigger

A person wants a stronger password.

## Outcome

The person signs in again everywhere with the new password.
