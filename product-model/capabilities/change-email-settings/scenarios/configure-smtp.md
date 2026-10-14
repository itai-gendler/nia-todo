---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Administrator enters the mail server, port, security, sender and link validity",
      "kind": "actor",
      "actor": "administrator",
      "entities": [
        {
          "entity": "instance-settings",
          "effect": "changes",
          "facts": [
            "Email delivery",
            "Password link validity"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::administration::email"
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
            "Email delivery",
            "Password link validity"
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

# Configure email delivery

## Trigger

The administrator wants invitations to go out by email.

## Outcome

The server sends its emails through that mail server.

## Edge cases

- Link validity must be between 1 and 168 hours.
