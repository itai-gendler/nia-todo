---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Administrator enters an address and sends a test",
      "kind": "actor",
      "actor": "administrator",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web-app::administration::email"
        }
      }
    },
    {
      "text": "The Product sends a test email through the configured mail server and reports success or the error",
      "kind": "product",
      "actor": "administrator",
      "entities": [
        {
          "entity": "instance-settings",
          "effect": "reads",
          "facts": [
            "Email delivery"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::administration::email"
        }
      }
    }
  ]
}
---

# Send a test email

## Trigger

The administrator just entered the mail settings.

## Outcome

The administrator knows whether email works.
