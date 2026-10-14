---
{
  "kind": "alternative",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User removes their avatar and confirms",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "user",
          "effect": "reads",
          "facts": [
            "Avatar"
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
      "text": "The Product deletes the avatar",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "user",
          "effect": "changes",
          "facts": [
            "Avatar"
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

# Remove the avatar

## Trigger

A person no longer wants a picture shown.

## Outcome

The person appears without an avatar.
