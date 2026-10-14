---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Administrator enters the current admin password and a new one",
      "kind": "actor",
      "actor": "administrator",
      "entities": [
        {
          "entity": "instance-settings",
          "effect": "changes",
          "facts": [
            "Admin password"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::administration"
        }
      }
    },
    {
      "text": "The Product saves the new admin password and ends every administration session",
      "kind": "product",
      "actor": "administrator",
      "entities": [
        {
          "entity": "instance-settings",
          "effect": "changes",
          "facts": [
            "Admin password"
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

# Change the admin password

## Trigger

The admin password may have been seen by someone else.

## Outcome

Only the new admin password opens administration; the administrator signs in again.

## Edge cases

- A wrong current admin password is refused.
