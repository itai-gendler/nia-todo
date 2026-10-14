---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User enters a new display name",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "user",
          "effect": "changes",
          "facts": [
            "Display name"
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
      "text": "The Product saves it",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "user",
          "effect": "changes",
          "facts": [
            "Display name"
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

# Change the display name

## Trigger

A person wants project members to see their full name.

## Outcome

The new name shows wherever the person appears.

## Edge cases

- A display name must not be empty and may have up to 80 characters.
