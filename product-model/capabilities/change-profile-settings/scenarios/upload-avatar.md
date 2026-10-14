---
{
  "kind": "alternative",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User chooses a JPEG, PNG, WebP, GIF or HEIC picture of up to 5 MB",
      "kind": "actor",
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
    },
    {
      "text": "The Product crops it to a square and saves it as the avatar",
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

# Upload an avatar

## Trigger

A person wants a picture next to their name.

## Outcome

The avatar shows wherever the person appears.

## Edge cases

- HEIC pictures are accepted only where the server can convert them.
