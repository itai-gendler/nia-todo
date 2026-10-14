---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Administrator enters the public HTTPS address and turns update analytics on or off",
      "kind": "actor",
      "actor": "administrator",
      "entities": [
        {
          "entity": "instance-settings",
          "effect": "changes",
          "facts": [
            "Public address",
            "Update analytics"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::administration::instance"
        }
      }
    },
    {
      "text": "The Product saves them",
      "kind": "product",
      "actor": "administrator",
      "entities": [
        {
          "entity": "instance-settings",
          "effect": "changes",
          "facts": [
            "Public address",
            "Update analytics"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::administration::instance"
        }
      }
    }
  ]
}
---

# Change the instance settings

## Trigger

The server moves behind a reverse proxy with its own domain.

## Outcome

Emailed links point at the new address.
