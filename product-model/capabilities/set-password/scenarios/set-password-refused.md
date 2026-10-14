---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User enters a password that does not meet the password rules",
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
          "place": "web-app::sign-in::set-password"
        }
      }
    },
    {
      "text": "The Product refuses and says what the password needs",
      "kind": "product",
      "actor": "user",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web-app::sign-in::set-password"
        }
      }
    }
  ]
}
---

# Choose a password that is too weak

## Trigger

A person picks a short password.

## Outcome

The link stays usable until the person chooses an acceptable password or it expires.
