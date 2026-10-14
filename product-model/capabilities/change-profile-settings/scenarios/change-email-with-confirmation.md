---
{
  "kind": "alternative",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User enters a new email address",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "user",
          "effect": "changes",
          "facts": [
            "Pending email"
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
      "text": "The server can send email",
      "kind": "condition",
      "actor": "user",
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
          "place": "web-app::app::profile-settings"
        }
      }
    },
    {
      "text": "The Product keeps the current address, records the new one as pending and emails it a confirmation link",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "user",
          "effect": "changes",
          "facts": [
            "Pending email"
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

# Change the email address with confirmation

## Trigger

A person moves to a new email provider.

## Outcome

The new address waits for confirmation; the old one stays in use until then.

## Edge cases

- An address another account already uses or waits for is refused without saying why.
- If the confirmation email cannot be sent, the address is not changed.
