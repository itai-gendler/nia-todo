---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Administrator enters the admin password",
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
      "text": "The Product checks it and opens the administration area",
      "kind": "product",
      "actor": "administrator",
      "entities": [
        {
          "entity": "instance-settings",
          "effect": "reads",
          "facts": [
            "Admin password",
            "Setup complete"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::administration"
        }
      }
    }
  ]
}
---

# Open the administration area

## Trigger

The administrator needs to add an account or change a server setting.

## Outcome

The administrator is in the administration area for up to a day.
