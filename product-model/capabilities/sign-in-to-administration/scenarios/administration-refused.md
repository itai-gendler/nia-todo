---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Administrator enters a wrong admin password",
      "kind": "actor",
      "actor": "administrator",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web-app::sign-in::admin-sign-in"
        }
      }
    },
    {
      "text": "The Product refuses",
      "kind": "product",
      "actor": "administrator",
      "entities": [
        {
          "entity": "instance-settings",
          "effect": "reads",
          "facts": [
            "Admin password"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::sign-in::admin-sign-in"
        }
      }
    }
  ]
}
---

# Enter a wrong admin password

## Trigger

The administrator mistypes the admin password.

## Outcome

The administration area stays closed; before first-run setup finishes it cannot be opened at all.
