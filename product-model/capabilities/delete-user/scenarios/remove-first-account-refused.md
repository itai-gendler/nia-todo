---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Administrator tries to delete the account created during first-run setup",
      "kind": "actor",
      "actor": "administrator",
      "entities": [
        {
          "entity": "user",
          "effect": "reads",
          "facts": [
            "Username",
            "First user"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::administration::users"
        }
      }
    },
    {
      "text": "The Product refuses",
      "kind": "product",
      "actor": "administrator",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web-app::administration::users"
        }
      }
    }
  ]
}
---

# Delete the first account

## Trigger

The administrator cleans up the list.

## Outcome

The first account stays.
