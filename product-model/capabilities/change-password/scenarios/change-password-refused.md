---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User enters a wrong current password",
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
      "text": "The Product refuses and keeps the old password",
      "kind": "product",
      "actor": "user",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web-app::app::security-settings"
        }
      }
    }
  ]
}
---

# Give a wrong current password

## Trigger

A person mistypes their current password.

## Outcome

Nothing changes.
